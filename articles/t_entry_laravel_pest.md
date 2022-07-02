---
title: "LaravelでPest入門"
emoji: "🐛"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["Laravel", "Pest", "UnitTest"]
published: true
---

## Pestとは？

https://pestphp.com/

[Pest](https://pestphp.com/)とは[Larastan](https://github.com/nunomaduro/larastan)や[Collision](https://github.com/nunomaduro/collision)などでお馴染みの[nunomaduro](https://github.com/nunomaduro)さんが携わっているPHPUnitの代替となる新しいテスティングフレームワークです。

PHPUnitの[Assertions](https://phpunit.readthedocs.io/ja/latest/assertions.html)が使え、更に独自で追加されたExpectationsによってよりシンプルに書くことが出来るようになっています。


### Jestの派生

[Jest](https://jestjs.io/ja/)を使った経験がある人であればPestはほとんどマスターしたと言えます。

`beforeEach()`や`test()`, `toBe()`, `expect()`そして`not`全て使えます。

Jestの`.`が`->`になった程度の違いくらいしか感じないでしょう。

### BDDフレームワーク

JestやPestはPHPUnitなどのxUnit系とは異なり、BDDを意識して作られたフレームワークです。

[BDD](https://circleci.com/ja/blog/how-to-test-software-part-ii-tdd-and-bdd/)の詳細な説明は省略しますが、「振る舞い」を検証することに主題を置いています。

モックを多用し、テストが単一クラスのみしか依存しなくなる状況にする手法は「振る舞い」というよりは「動作」検証になるでしょう。

「振る舞い」なので外部から観測できない部分に対してテストコードは書きません。(プライベートメソッドなど)

つまりpublicなメソッド(API)に対してテストを書いていきます。

## 使い方

### インストール

https://pestphp.com/docs/installation

composerにインストールやり方で特に変わりはありません。

```sh
composer require pestphp/pest-plugin-laravel --dev
```

インストール後に`artisan`を使用して別途インストールする必要があります。

```sh
php artisan pest:install
```

これは`tests/Pest.php`を作成する作業であり、この`Pest.php`は`TestCase::class`や`CreatesApplication::class`, `RefreshDatabase::class`を書いてディレクトリごとに適応したり、全体的に使うヘルパーメソッドを定義するグローバルな空間になります。

### testとit

https://pestphp.com/docs/writing-tests

Pestにはクラスを使う必要がなく、全て関数で完結します。

```php
class PostTest extends TestCase
{
	public function test_something(): void
	{
		...
	}
}
```

PHPUnitで上のようなクラスが必要であったテストも関数で簡単に書くことができます。

```php
test('test_something', function() {
	...
});

test('test_something')->toBe(...);
```

また、この`test()`関数以外に`it()`関数を使うことができます。

動作上はどちらでも変わりません。`it()`だと実行時テスト名に勝手に`it`が補完されるだけです。英語でテスト名を書いてく分には良いですが、日本語で書くルールがあるプロジェクトでは`test()`で書いていく方が無難だと思います。

### usesとbeforeEach

https://pestphp.com/docs/underlying-test-case

少し前述しましたが、`Pest.php`でテストを実行する前に行う動作を指定できます。

Laravelのテストではお馴染みの`TestCase`, `CreatesApplication`, `RefreshDatabase`をUnitディレクトリとFeatureディレクトリに適用させる場合は`uses`と`in`を使います。

```php
uses(TestCase::class, CreatesApplication::class, RefreshDatabase::class)
	->in('Unit', 'Feature')
```

外部プロセス依存になるモック等は`beforeEach()`で指定すると適用することができます。

```php
uses(TestCase::class, CreatesApplication::class, RefreshDatabase::class)
	->beforeEach(function() {
		Bus::fake(SampleJob::class)
	})
	->in('Unit', 'Feature')
```

### AssertionsとExpectations

#### Assertions

https://pestphp.com/docs/assertions

PHPUnitでお馴染みの[Assertions](https://phpunit.readthedocs.io/ja/latest/assertions.html)が使用できます。

ただPestでAssertionsは補助的な意味合いが強く、Expectationsを使うことによって真価が発揮されるものだと思っているので、なるべくExpectationsを使う方が良いと思います。

Laravel特有の`assertDatabaseHas`や`assertStatus`は頼るしかないので、変にやりくりしようとせずにAssertで済ませましょう。

#### Expectations

https://pestphp.com/docs/expectations

Jestではお馴染みのExpectationsです。公式ドキュメントからの引用ですが
```php
test('expect true to be true', function () {

// assertion

$this->assertTrue(true);

// expectation

expect(true)->toBe(true);

});
```

とexpectの場合はメソッドチェーンで書くことができます。

つまり、1つの要素を様々な観点からAssertionする時に何行にも渡って似たような文を書かないといけませんでしたが、それがなくなることになります。

```php
$a = 1;
$this->assertEqulas($a, 1);
$this->assertInt($a);
// ...

expect($a)
	->toBe(1)
	->toBeInt();
// Done!
```

一つの要素から枝分かれしていることが瞬時に分かるため、テストの可読性が大きく向上することになります。

テストはメンテナンスされていくべきものであり（工数があれば本番コード同等と扱うべきもの）、テストは使い捨てではないため、可読性は重要です。Pestはその手伝いをしてくれることになるでしょう。

細かいExpectationsは公式ドキュメントをお読みください。ここで説明しきれないほど様々な種類のExpectationsが用意されています。

### High Order Tests

https://pestphp.com/docs/higher-order-tests

 基本的にメソッドチェーンができます。

例えば、あるPostについていくつか検証したい時は以下のように続けて検査することができます。
```php
$post = Post::factory()->create();

$refreshPost = $post->refresh();

expect($refreshPost)
	->title->toBe($requestData['title'])
	->author->toBe($requestData['author'])
	->body->toBe($requestData['body'])
	->date->toBe($requestData['date']);

```

メソッドチェーンはテストメソッドの `it()`や `test()`にも有効です。
公式Docからの引用です。

```php

test('the user has the correct values')
	->expect(fn() => Auth::user())
	->first_name->toEqual('Nuno')
	->last_name->toEqual('Maduro')
	->withTitle('Mr')->toEqual('Mr Nuno Maduro');
```

### Exceptions

https://pestphp.com/docs/exceptions-and-errors

PHPUnitでは `$this->expectException()`を使って例外を検査しますが、Pestではメソッドチェーンで書きます。(以下公式Doc引用)

```php

it('throws exception', function () {
	throw new Exception('Something happened.');
})->throws(Exception::class);

```

### Datasets

https://pestphp.com/docs/datasets

PHPUnitのところのData Providerに近いものとなります。

基本的にはテストメソッド`it()`や`test()`にチェーンで繋げて、引数に渡す要素を設定します。(公式Docから引用)

```php

it('has emails', function ($name, $email) {
	expect($email)->not->toBeEmpty();
})->with([
	['Nuno', 'enunomaduro@gmail.com'],
	['Other', 'other@example.com']
]);
```

また、別ファイルに`dataset()`で定義して、それを利用することができます。（テストメソッドとテストデータの距離が遠くなって個人的には可読性が落ちるので好きではないです）

公式Docから引用
```php
<?php
dataset('emails', [
	'enunomaduro@gmail.com',
	'other@example.com'
]);
```

### Custom Factory

RequestデータやJsonカラムなどがある場合、事前データが膨大になってテストメソッドの見通しが悪くなり、可読性が落ちたり、単純にいちいち要素を指定して事前データを作成するのが面倒だと感じるときがあります。

その際にカスタムファクトリーを作っています。

```php
<?php
namespace Tests\Factories;
use App\Models\BlogPost;
use Carbon\Carbon;

class BlogPostRequestDataFactory
{
	private string $title = 'Title';
	private string $author = 'Author';
	private string $body = 'Body';
	private string $date = '2021-01-01';

	public static function new(): self
	{
		return new self();
	}

	public function create(array $extra = []): array
	{
		return $extra + [
			'title' => $this->title,
			'author' => $this->author,
			'body' => $this->body,
			'date' => $this->date,
		];
	}

	public function withTitle(string $title): self
	{
		$clone = clone $this;
		$clone->title = $title;
		return $clone;
	}

	public function withDate(string|Carbon $date): self
	{
		$clone = clone $this;
		$clone->date = $date instanceof Carbon
			? $date->format('Y-m-d')
			: $date;
		return $clone;
	}

	public function withPost(BlogPost $post): self
	{

		$clone = clone $this;
		$this->title = $post->title;
		$this->author = $post->author;
		$this->body = $post->body;
		$this->date = $post->date->format('Y-m-d');
		return $clone;
	}

}
```

基本的に`beforeEach()`、`setUp()`で `new()`しておき、インスタンス変数として格納しておき、それにwithXXXメソッドで属性を保管しつつ、create()するというのが主な使い方になります。

### Time Freeze

別途プラグインがあります。`Carbon::setTestNow()`のイメージです。
```sh
composer require spatie/pest-plugin-test-time --dev
```

テストを行う際に年月日時刻はできれば特定の年月日時刻にしておきたいです。
Carbonのように扱え、更に設定した時刻を簡単に操作出来るので便利です。

公式Docから引用
```php
testTime()->freeze('2021-01-02 12:34:56');
testTime()->addHour();
testTime()->subMinute()->addSeconds(2);
```

### Validation Test

https://readouble.com/laravel/8.x/ja/http-tests.html#assert-session-has-errors

以前Requestクラスにルールの検証としてdataProviderを使っていましたが、`assertSessionHasErrors()`を使えばスマートに検証ができます。

Errorが出るものを指定します。
例えば、`title => required, string`だったら、データがなかった時にerrorが出るので、`assertSessionHasErrors(['title'])`とすればPassする

```php
$post = Post::factory()->create();

post(action([BlogPostAdminController::class, 'update'], 			$post->slug), [
])
	->assertSessionHasErrors(['title', 'author', 'body', 'date']);
```

`dumpSession()` を使ってセッション情報をdumpし、`assertSessionHasErrors`の引数arrayに連想配列でkey とメッセージを指定すると分かりやすい。

```php
post(action([BlogPostAdminController::class, 'update'], $post->slug), [
	'title' => $post->title
	'author' => $post->author,
	'body' => $post->body,
	'date' => '01/01/2021',
])->dumpSession()->assertSessionHasErrors([
	'date' => 'The date does not match the format Y-m-d.'
])
```

### Json Test

https://readouble.com/laravel/8.x/ja/http-tests.html#fluent-json-testing

APIのテストを書いている時にレスポンスをある程度検証したい場合があります。ただ `assertJson`だとイマイチ使いづらい・・・。ってなった時にClosureで指定して上げると楽になります。

```php
it('xxx', function() {
	$post = BlogPost::factory()->count(5)->create();
	
	$returnedPosts = getJson(action([BlogPostController::class, 'index']))
		->assertSuccessful()
		->assertJsonCount(5, 'data')
		->assertJson(function(AssertableJson $json) {
			$json->has('data', 5)
				->has('data.0', function(AssertableJson $json) {
					$json
						->where('id', $posts[0]->id)
						->where('slug', $posts[0]->slug)
						->has('date', $posts[0]->date->toDateTimeLocalString)
						->whereAllType([
							'id' => 'integer',
							'slug' => 'string',
							'date' => 'string',
						])
						->etc();
				})
		})	
		
});
```


### Custom Expectations

ほかのテストでも長いExpectationsを書くのは面倒です。

その場合用の自分で定義できるExpectationsがあります。

`extend`で指定するだけで自分だけのExpectationsが作成できます。自分だけのExpectationsを見つけて、最強のExpectationsを育てろ！

```php
expect(5)->toBeInTheRange(1, 10);

expect()->extend('toBeInTheRange', function(int $min, int $max) {
	return $this
		->toBeGreaterThanOrEqual($min)
		->toBeLessThanOrEqual($max);
});
```

### IDEプラグイン

プラグインダウンロード数だけ見るとめちゃくちゃマイナーなことがわかりますね・・・。

https://plugins.jetbrains.com/plugin/14636-pest

https://marketplace.visualstudio.com/items?itemName=m1guelpf.better-pest

https://marketplace.visualstudio.com/items?itemName=dansysanalyst.pest-snippets

## 参考

### 公式

https://pestphp.com/

公式になります。


### 教科書

https://testing-laravel.com/

テストTipsで発見があります。
