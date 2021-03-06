---
title: "Laravelã§Pestå¥é"
emoji: "ð"
type: "tech" # tech: æè¡è¨äº / idea: ã¢ã¤ãã¢
topics: ["Laravel", "Pest", "UnitTest"]
published: true
---

## Pestã¨ã¯ï¼

https://pestphp.com/

[Pest](https://pestphp.com/)ã¨ã¯[Larastan](https://github.com/nunomaduro/larastan)ã[Collision](https://github.com/nunomaduro/collision)ãªã©ã§ãé¦´æã¿ã®[nunomaduro](https://github.com/nunomaduro)ãããæºãã£ã¦ããPHPUnitã®ä»£æ¿ã¨ãªãæ°ãããã¹ãã£ã³ã°ãã¬ã¼ã ã¯ã¼ã¯ã§ãã

PHPUnitã®[Assertions](https://phpunit.readthedocs.io/ja/latest/assertions.html)ãä½¿ããæ´ã«ç¬èªã§è¿½å ãããExpectationsã«ãã£ã¦ããã·ã³ãã«ã«æ¸ããã¨ãåºæ¥ãããã«ãªã£ã¦ãã¾ãã


### Jestã®æ´¾ç

[Jest](https://jestjs.io/ja/)ãä½¿ã£ãçµé¨ãããäººã§ããã°Pestã¯ã»ã¨ãã©ãã¹ã¿ã¼ããã¨è¨ãã¾ãã

`beforeEach()`ã`test()`, `toBe()`, `expect()`ããã¦`not`å¨ã¦ä½¿ãã¾ãã

Jestã®`.`ã`->`ã«ãªã£ãç¨åº¦ã®éããããããæããªãã§ãããã

### BDDãã¬ã¼ã ã¯ã¼ã¯

JestãPestã¯PHPUnitãªã©ã®xUnitç³»ã¨ã¯ç°ãªããBDDãæè­ãã¦ä½ããããã¬ã¼ã ã¯ã¼ã¯ã§ãã

[BDD](https://circleci.com/ja/blog/how-to-test-software-part-ii-tdd-and-bdd/)ã®è©³ç´°ãªèª¬æã¯çç¥ãã¾ããããæ¯ãèãããæ¤è¨¼ãããã¨ã«ä¸»é¡ãç½®ãã¦ãã¾ãã

ã¢ãã¯ãå¤ç¨ãããã¹ããåä¸ã¯ã©ã¹ã®ã¿ããä¾å­ããªããªãç¶æ³ã«ããææ³ã¯ãæ¯ãèããã¨ããããã¯ãåä½ãæ¤è¨¼ã«ãªãã§ãããã

ãæ¯ãèãããªã®ã§å¤é¨ããè¦³æ¸¬ã§ããªãé¨åã«å¯¾ãã¦ãã¹ãã³ã¼ãã¯æ¸ãã¾ããã(ãã©ã¤ãã¼ãã¡ã½ãããªã©)

ã¤ã¾ãpublicãªã¡ã½ãã(API)ã«å¯¾ãã¦ãã¹ããæ¸ãã¦ããã¾ãã

## ä½¿ãæ¹

### ã¤ã³ã¹ãã¼ã«

https://pestphp.com/docs/installation

composerã«ã¤ã³ã¹ãã¼ã«ããæ¹ã§ç¹ã«å¤ããã¯ããã¾ããã

```sh
composer require pestphp/pest-plugin-laravel --dev
```

ã¤ã³ã¹ãã¼ã«å¾ã«`artisan`ãä½¿ç¨ãã¦å¥éã¤ã³ã¹ãã¼ã«ããå¿è¦ãããã¾ãã

```sh
php artisan pest:install
```

ããã¯`tests/Pest.php`ãä½æããä½æ¥­ã§ããããã®`Pest.php`ã¯`TestCase::class`ã`CreatesApplication::class`, `RefreshDatabase::class`ãæ¸ãã¦ãã£ã¬ã¯ããªãã¨ã«é©å¿ããããå¨ä½çã«ä½¿ããã«ãã¼ã¡ã½ãããå®ç¾©ããã°ã­ã¼ãã«ãªç©ºéã«ãªãã¾ãã

### testã¨it

https://pestphp.com/docs/writing-tests

Pestã«ã¯ã¯ã©ã¹ãä½¿ãå¿è¦ããªããå¨ã¦é¢æ°ã§å®çµãã¾ãã

```php
class PostTest extends TestCase
{
	public function test_something(): void
	{
		...
	}
}
```

PHPUnitã§ä¸ã®ãããªã¯ã©ã¹ãå¿è¦ã§ãã£ããã¹ããé¢æ°ã§ç°¡åã«æ¸ããã¨ãã§ãã¾ãã

```php
test('test_something', function() {
	...
});

test('test_something')->toBe(...);
```

ã¾ãããã®`test()`é¢æ°ä»¥å¤ã«`it()`é¢æ°ãä½¿ããã¨ãã§ãã¾ãã

åä½ä¸ã¯ã©ã¡ãã§ãå¤ããã¾ããã`it()`ã ã¨å®è¡æãã¹ãåã«åæã«`it`ãè£å®ãããã ãã§ããè±èªã§ãã¹ãåãæ¸ãã¦ãåã«ã¯è¯ãã§ãããæ¥æ¬èªã§æ¸ãã«ã¼ã«ããããã­ã¸ã§ã¯ãã§ã¯`test()`ã§æ¸ãã¦ããæ¹ãç¡é£ã ã¨æãã¾ãã

### usesã¨beforeEach

https://pestphp.com/docs/underlying-test-case

å°ãåè¿°ãã¾ãããã`Pest.php`ã§ãã¹ããå®è¡ããåã«è¡ãåä½ãæå®ã§ãã¾ãã

Laravelã®ãã¹ãã§ã¯ãé¦´æã¿ã®`TestCase`, `CreatesApplication`, `RefreshDatabase`ãUnitãã£ã¬ã¯ããªã¨Featureãã£ã¬ã¯ããªã«é©ç¨ãããå ´åã¯`uses`ã¨`in`ãä½¿ãã¾ãã

```php
uses(TestCase::class, CreatesApplication::class, RefreshDatabase::class)
	->in('Unit', 'Feature')
```

å¤é¨ãã­ã»ã¹ä¾å­ã«ãªãã¢ãã¯ç­ã¯`beforeEach()`ã§æå®ããã¨é©ç¨ãããã¨ãã§ãã¾ãã

```php
uses(TestCase::class, CreatesApplication::class, RefreshDatabase::class)
	->beforeEach(function() {
		Bus::fake(SampleJob::class)
	})
	->in('Unit', 'Feature')
```

### Assertionsã¨Expectations

#### Assertions

https://pestphp.com/docs/assertions

PHPUnitã§ãé¦´æã¿ã®[Assertions](https://phpunit.readthedocs.io/ja/latest/assertions.html)ãä½¿ç¨ã§ãã¾ãã

ãã Pestã§Assertionsã¯è£å©çãªæå³åããå¼·ããExpectationsãä½¿ããã¨ã«ãã£ã¦çä¾¡ãçºæ®ããããã®ã ã¨æã£ã¦ããã®ã§ããªãã¹ãExpectationsãä½¿ãæ¹ãè¯ãã¨æãã¾ãã

Laravelç¹æã®`assertDatabaseHas`ã`assertStatus`ã¯é ¼ããããªãã®ã§ãå¤ã«ãããããããã¨ããã«Assertã§æ¸ã¾ãã¾ãããã

#### Expectations

https://pestphp.com/docs/expectations

Jestã§ã¯ãé¦´æã¿ã®Expectationsã§ããå¬å¼ãã­ã¥ã¡ã³ãããã®å¼ç¨ã§ãã
```php
test('expect true to be true', function () {

// assertion

$this->assertTrue(true);

// expectation

expect(true)->toBe(true);

});
```

ã¨expectã®å ´åã¯ã¡ã½ãããã§ã¼ã³ã§æ¸ããã¨ãã§ãã¾ãã

ã¤ã¾ãã1ã¤ã®è¦ç´ ãæ§ããªè¦³ç¹ããAssertionããæã«ä½è¡ã«ãæ¸¡ã£ã¦ä¼¼ããããªæãæ¸ããªãã¨ããã¾ããã§ããããããããªããªããã¨ã«ãªãã¾ãã

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

ä¸ã¤ã®è¦ç´ ããæåãããã¦ãããã¨ãç¬æã«åããããããã¹ãã®å¯èª­æ§ãå¤§ããåä¸ãããã¨ã«ãªãã¾ãã

ãã¹ãã¯ã¡ã³ããã³ã¹ããã¦ããã¹ããã®ã§ããï¼å·¥æ°ãããã°æ¬çªã³ã¼ãåç­ã¨æ±ãã¹ããã®ï¼ããã¹ãã¯ä½¿ãæ¨ã¦ã§ã¯ãªããããå¯èª­æ§ã¯éè¦ã§ããPestã¯ãã®æä¼ãããã¦ããããã¨ã«ãªãã§ãããã

ç´°ããExpectationsã¯å¬å¼ãã­ã¥ã¡ã³ãããèª­ã¿ãã ãããããã§èª¬æããããªãã»ã©æ§ããªç¨®é¡ã®Expectationsãç¨æããã¦ãã¾ãã

### High Order Tests

https://pestphp.com/docs/higher-order-tests

 åºæ¬çã«ã¡ã½ãããã§ã¼ã³ãã§ãã¾ãã

ä¾ãã°ãããPostã«ã¤ãã¦ããã¤ãæ¤è¨¼ãããæã¯ä»¥ä¸ã®ããã«ç¶ãã¦æ¤æ»ãããã¨ãã§ãã¾ãã
```php
$post = Post::factory()->create();

$refreshPost = $post->refresh();

expect($refreshPost)
	->title->toBe($requestData['title'])
	->author->toBe($requestData['author'])
	->body->toBe($requestData['body'])
	->date->toBe($requestData['date']);

```

ã¡ã½ãããã§ã¼ã³ã¯ãã¹ãã¡ã½ããã® `it()`ã `test()`ã«ãæå¹ã§ãã
å¬å¼Docããã®å¼ç¨ã§ãã

```php

test('the user has the correct values')
	->expect(fn() => Auth::user())
	->first_name->toEqual('Nuno')
	->last_name->toEqual('Maduro')
	->withTitle('Mr')->toEqual('Mr Nuno Maduro');
```

### Exceptions

https://pestphp.com/docs/exceptions-and-errors

PHPUnitã§ã¯ `$this->expectException()`ãä½¿ã£ã¦ä¾å¤ãæ¤æ»ãã¾ãããPestã§ã¯ã¡ã½ãããã§ã¼ã³ã§æ¸ãã¾ãã(ä»¥ä¸å¬å¼Docå¼ç¨)

```php

it('throws exception', function () {
	throw new Exception('Something happened.');
})->throws(Exception::class);

```

### Datasets

https://pestphp.com/docs/datasets

PHPUnitã®ã¨ããã®Data Providerã«è¿ããã®ã¨ãªãã¾ãã

åºæ¬çã«ã¯ãã¹ãã¡ã½ãã`it()`ã`test()`ã«ãã§ã¼ã³ã§ç¹ãã¦ãå¼æ°ã«æ¸¡ãè¦ç´ ãè¨­å®ãã¾ãã(å¬å¼Docããå¼ç¨)

```php

it('has emails', function ($name, $email) {
	expect($email)->not->toBeEmpty();
})->with([
	['Nuno', 'enunomaduro@gmail.com'],
	['Other', 'other@example.com']
]);
```

ã¾ããå¥ãã¡ã¤ã«ã«`dataset()`ã§å®ç¾©ãã¦ããããå©ç¨ãããã¨ãã§ãã¾ããï¼ãã¹ãã¡ã½ããã¨ãã¹ããã¼ã¿ã®è·é¢ãé ããªã£ã¦åäººçã«ã¯å¯èª­æ§ãè½ã¡ãã®ã§å¥½ãã§ã¯ãªãã§ãï¼

å¬å¼Docããå¼ç¨
```php
<?php
dataset('emails', [
	'enunomaduro@gmail.com',
	'other@example.com'
]);
```

### Custom Factory

Requestãã¼ã¿ãJsonã«ã©ã ãªã©ãããå ´åãäºåãã¼ã¿ãè¨å¤§ã«ãªã£ã¦ãã¹ãã¡ã½ããã®è¦éããæªããªããå¯èª­æ§ãè½ã¡ãããåç´ã«ãã¡ãã¡è¦ç´ ãæå®ãã¦äºåãã¼ã¿ãä½æããã®ãé¢åã ã¨æããã¨ããããã¾ãã

ãã®éã«ã«ã¹ã¿ã ãã¡ã¯ããªã¼ãä½ã£ã¦ãã¾ãã

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

åºæ¬çã«`beforeEach()`ã`setUp()`ã§ `new()`ãã¦ãããã¤ã³ã¹ã¿ã³ã¹å¤æ°ã¨ãã¦æ ¼ç´ãã¦ãããããã«withXXXã¡ã½ããã§å±æ§ãä¿ç®¡ãã¤ã¤ãcreate()ããã¨ããã®ãä¸»ãªä½¿ãæ¹ã«ãªãã¾ãã

### Time Freeze

å¥éãã©ã°ã¤ã³ãããã¾ãã`Carbon::setTestNow()`ã®ã¤ã¡ã¼ã¸ã§ãã
```sh
composer require spatie/pest-plugin-test-time --dev
```

ãã¹ããè¡ãéã«å¹´ææ¥æå»ã¯ã§ããã°ç¹å®ã®å¹´ææ¥æå»ã«ãã¦ããããã§ãã
Carbonã®ããã«æ±ããæ´ã«è¨­å®ããæå»ãç°¡åã«æä½åºæ¥ãã®ã§ä¾¿å©ã§ãã

å¬å¼Docããå¼ç¨
```php
testTime()->freeze('2021-01-02 12:34:56');
testTime()->addHour();
testTime()->subMinute()->addSeconds(2);
```

### Validation Test

https://readouble.com/laravel/8.x/ja/http-tests.html#assert-session-has-errors

ä»¥åRequestã¯ã©ã¹ã«ã«ã¼ã«ã®æ¤è¨¼ã¨ãã¦dataProviderãä½¿ã£ã¦ãã¾ãããã`assertSessionHasErrors()`ãä½¿ãã°ã¹ãã¼ãã«æ¤è¨¼ãã§ãã¾ãã

Errorãåºããã®ãæå®ãã¾ãã
ä¾ãã°ã`title => required, string`ã ã£ããããã¼ã¿ããªãã£ãæã«errorãåºãã®ã§ã`assertSessionHasErrors(['title'])`ã¨ããã°Passãã

```php
$post = Post::factory()->create();

post(action([BlogPostAdminController::class, 'update'], 			$post->slug), [
])
	->assertSessionHasErrors(['title', 'author', 'body', 'date']);
```

`dumpSession()` ãä½¿ã£ã¦ã»ãã·ã§ã³æå ±ãdumpãã`assertSessionHasErrors`ã®å¼æ°arrayã«é£æ³éåã§key ã¨ã¡ãã»ã¼ã¸ãæå®ããã¨åãããããã

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

APIã®ãã¹ããæ¸ãã¦ããæã«ã¬ã¹ãã³ã¹ãããç¨åº¦æ¤è¨¼ãããå ´åãããã¾ãããã  `assertJson`ã ã¨ã¤ãã¤ãä½¿ãã¥ããã»ã»ã»ãã£ã¦ãªã£ãæã«Closureã§æå®ãã¦ä¸ããã¨æ¥½ã«ãªãã¾ãã

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

ã»ãã®ãã¹ãã§ãé·ãExpectationsãæ¸ãã®ã¯é¢åã§ãã

ãã®å ´åç¨ã®èªåã§å®ç¾©ã§ããExpectationsãããã¾ãã

`extend`ã§æå®ããã ãã§èªåã ãã®Expectationsãä½æã§ãã¾ããèªåã ãã®Expectationsãè¦ã¤ãã¦ãæå¼·ã®Expectationsãè²ã¦ãï¼

```php
expect(5)->toBeInTheRange(1, 10);

expect()->extend('toBeInTheRange', function(int $min, int $max) {
	return $this
		->toBeGreaterThanOrEqual($min)
		->toBeLessThanOrEqual($max);
});
```

### IDEãã©ã°ã¤ã³

ãã©ã°ã¤ã³ãã¦ã³ã­ã¼ãæ°ã ãè¦ãã¨ãã¡ããã¡ããã¤ãã¼ãªãã¨ããããã¾ãã­ã»ã»ã»ã

https://plugins.jetbrains.com/plugin/14636-pest

https://marketplace.visualstudio.com/items?itemName=m1guelpf.better-pest

https://marketplace.visualstudio.com/items?itemName=dansysanalyst.pest-snippets

## åè

### å¬å¼

https://pestphp.com/

å¬å¼ã«ãªãã¾ãã


### æç§æ¸

https://testing-laravel.com/

ãã¹ãTipsã§çºè¦ãããã¾ãã
