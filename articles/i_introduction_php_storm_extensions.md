---
title: "【随時更新】PhpStormのおすすめの拡張機能"
emoji: "🙏"
type: "idea" # tech: 技術記事 / idea: アイデア
topics: ["PHPStorm", "プラグイン", "ツール"]
published: true
---

## ネタ系

###  Nyan Progress Bar 

https://plugins.jetbrains.com/plugin/8575-nyan-progress-bar


PhpStormに使われるプログレスバーをNyanCatに置き換えます。かわいい。
プログレスバーはインデックス作成の時にも出てくるので頻繁に目にします。癒やしを求めてください。

他にも Progre Barを置き換えるプラグインはたくさんあるので、好きなものを使ってください。

https://plugins.jetbrains.com/plugin/14708-mario-progress-bar

https://plugins.jetbrains.com/plugin/11602-duck-progress-bar

https://plugins.jetbrains.com/plugin/14609-pokemon-trainer-progress-bar

https://plugins.jetbrains.com/plugin/12453-hadouken-progress-bar

https://plugins.jetbrains.com/plugin/14604-eevee-progress-bar

https://plugins.jetbrains.com/plugin/15291-elephpant-progress-bar


### Nyan Tray

https://plugins.jetbrains.com/plugin/11286-nyan-tray

MacのメニューバーにPhpStormのパフォーマンス状況をNyanCatで教えてくれます。~~正直いらないかも~~

## 便利系

あると便利なのでぜひとも導入したいプラグインが多いです。

### .env files support

https://plugins.jetbrains.com/plugin/9525--env-files-support

.envファイルを編集しやすくしてくれます（補完やカラーリングなど）。
地味ですが外せないプラグインの1つだと思っています。

###  .ignore

https://plugins.jetbrains.com/plugin/7495--ignore

.ignoreファイルを簡単にテンプレートから選ぶことで作成ができます。
ターミナルツール等で似たようなものはありますが、PhpStormでサクッと作りたい時に便利です。

###  CSV

https://plugins.jetbrains.com/plugin/10037-csv

CSVファイルを見やすくします。これだけで十分です。

###  deep-assoc-completion

https://plugins.jetbrains.com/plugin/9927-deep-assoc-completion

PHPの連想配列に補完が効くようになります。これだけ聞くと地味そうに感じるのですが、めちゃくちゃ便利です。

自分の中でも割とベストに入るくらい便利なプラグインだと感じています。

###  GitToolBox

https://plugins.jetbrains.com/plugin/7499-gittoolbox

Gitを使いやすくしてくれます。自動フェッチ・ブランチ名補完・ブランチ切り替え簡略化など足回りが良くなります。

ディレクトリ表示の横に現在ブランチを出してくれるので、複数のリポジトリをまたがる際に非常に便利です。

###  Japanese Language Pack / 日本語言語パック

https://plugins.jetbrains.com/plugin/13964-japanese-language-pack------

母国語なので安心します。細かい設定も英語から日本語になるので非常に助かります。
これがなかったらPhpStormの設定を1個1個見ようなんて思いませんでした。

###  PHP Annotations

https://plugins.jetbrains.com/plugin/7320-php-annotations


###  Php Inspections (EA Extended)

https://plugins.jetbrains.com/plugin/7622-php-inspections-ea-extended-

PHPを書く上で、バグを引き起こすかもしれない部分に警告文を出してくれます。

PHPStanとはまた草分けが違い、if文で「この条件おかしくない？」とか「emptyでいいの？nullのがよくない？」みたいな助言をしてくれます。

インスペクションでサクッと適切な形に自動整形してくれるので便利で手放せません。

１行関数をArrow Functionに変えるのも簡単に整形してくれるので楽です。
ぜひ入れていただきたいプラグインです。

###  Rainbow Brackets

https://plugins.jetbrains.com/plugin/10080-rainbow-brackets

ブラケットは光らせましょう。それだけで視認性が大きく変わり、効率が違います。そういえばVS Codeはデフォルトになりましたね。

###  SonarLint

https://plugins.jetbrains.com/plugin/7973-sonarlint

Lintしてくれます。 Php Inspections (EA Extended)とは別ベクトルで怒ってくれる為、2個とも入れればベテランエンジニア2人とモブプロしている気分になります

### String Manipulation

https://plugins.jetbrains.com/plugin/2162-string-manipulation

キャメルケースだのスネークケースだのなんだのを一発で変換してくれるプラグインです。

### OpenAPI(Swagger) Editor

https://plugins.jetbrains.com/plugin/14837-openapi-swagger-editor

文字通りOpenAPI Editorです。Stoplightも使うときもありますが、ササッと修正だけしたい場合には便利です！

### Makefile Language

https://plugins.jetbrains.com/plugin/9333-makefile-language

MakefileをSyntax Highlightしたり、補完が効くやつになります。

割と面倒なのをMakefileで書いてしまうので重宝しています。

### Conventional Commit & # Commitlint Conventional Commit

https://www.conventionalcommits.org/en/v1.0.0/

コミットを読みやすくするためのルールとしてconventional commitsがあると思います。

https://plugins.jetbrains.com/plugin/13389-conventional-commit

これはconventional commitsに則ったようにコミットメッセージを組み立てられるように補助してくれるプラグインになります。

ダイアログが出るので、それに入力していくだけで組み立てられるため、構造やルールを覚える必要がなくなります。

また、Lintとしてルールを徹底させたい場合はLintとして以下のプラグインが役煮立ちます。

https://github.com/conventional-changelog/commitlint

https://plugins.jetbrains.com/plugin/14046-commitlint-conventional-commit


### Active Tab Highlighter

https://plugins.jetbrains.com/plugin/9562-active-tab-highlighter

Icebergテーマを使用していると高頻度で「あれ、今どれ開いてるんだっけ」というのがわからなくなってしまうので入れてます。

###  Tabnine AI Code Completion- JS Java Python TS Rust Go PHP & More

https://plugins.jetbrains.com/plugin/12798-tabnine-ai-code-completion-js-java-python-ts-rust-go-php--more

---

ちまたでは[GitHub Copilot](https://copilot.github.com/)が有名ですが、自分はあれがお節介すぎるのとタブ補完が少し使いづらくなるので苦手でした。

Tabnineはタブ補完で予測を出してくれる上に、ファイル上からも予測を行なってくれます。似たような文が続くテストコード等では大活躍で、少し癖はあるものの、効率は大幅に向上します。ぜひ利用して欲しいプラグインです。

Tabnineはかなり重宝しています。
補完が効かない場所もAIによって補完を出してくれる場合があったり、連想配列のkeyもサクッと予測してくれるのでかなり便利です。

統計も出るので、どれくらい自動化されたのかが分かりやすいです。
自分は15%くらいです。

---


###  Translation

https://plugins.jetbrains.com/plugin/8579-translation

Google翻訳を楽に行えます。

本領発揮をするのは**メソッドとかにカーソルを置いてると出てくるポップアップとかにも簡単に翻訳を掛けられることです。**

ライブラリのコメントは英語で書かれていることが多いので、重宝します。

###  PlantUML integration

https://plugins.jetbrains.com/plugin/7017-plantuml-integration

モデリングする時や思考を整理するためにPlantUMLを書くことがあるのですが、PhpStorm上で書けるようになるので便利です。

## 操作系

###  IdeaVim
https://plugins.jetbrains.com/plugin/164-ideavim

PhpStormの操作をvim配列にします。
vimを使わない人には必要ないですが、vimを使う人には命よりも大切なプラグインになります。

###  IdeaVim-EasyMotion

https://plugins.jetbrains.com/plugin/13360-ideavim-easymotion

EasyMotionを使用できるようにします。後述のAceJumpをラップしてるだけっぽいので、AceJumpのキーコンフィグを変更して、大人しくAceJumpを使ってもいいかもしれません。

###  AceJump

https://plugins.jetbrains.com/plugin/7086-acejump

vimで言うようなeasy-motion, VS Codeだとjumpyみたいな動作を提供してくれます。

###  Key Promoter X

https://plugins.jetbrains.com/plugin/9792-key-promoter-x

ショートカットキーがあるのにGUI操作すると怒ってくるお母さん系プラグインです。
たしかに「ほーん」とはなるのですが、無視してGUI操作することがあります。癖って怖いですね。

## テーマ系

### Atom Material Icons

https://plugins.jetbrains.com/plugin/10044-atom-material-icons

デフォルトのアイコンは見づらく視認性が悪いです。なのでこのAtom Material Iconsを入れて瞬時に判断しやすくします。
アイコンの見やすさは個人的に重要なのでマストです。

###  Iceberg

https://plugins.jetbrains.com/plugin/15126-iceberg

個人的にカラーテーマはIcebergが見やすいと思っているのでIcebergで統一しています。シンプルに目に優しくて見やすいです。

###  The Doki Theme

https://plugins.jetbrains.com/plugin/10804-the-doki-theme

IceBergかこっちがテーマの筆頭となります。最近はゆるキャンのキャラが追加されたとか。

ちなみに[テスト実行時やビルド時にアニメワンカットシーンが流れるイカれたプラグイン](https://plugins.jetbrains.com/plugin/15865-anime-memes)も出てます。~~一時期入れてみましたがうるさくて邪魔です~~
にしても海外のアニメオタクの情熱はすごいですね・・・。

## Laravel系

Laravelを書く際に便利な拡張機能です。

### Collector

https://plugins.jetbrains.com/plugin/15246-collector

Laravelの組み込みである`collection`を便利に使えるようになります。

###  Laravel Idea

https://plugins.jetbrains.com/plugin/13441-laravel-idea

サブスクリプションが必要なプラグインになるのでオススメしづらいですが、RequestのRulesで補完が効くようになったり、簡単にartisanを使わなくてもファイル作成ができ便利です。
他にも機能はありますが詳しくは[こっち](https://laravel-idea.com/docs/overview)を見た方が早いです。

###  Laravel Query

https://plugins.jetbrains.com/plugin/16309-laravel-query

Laravelでのクエリ部分を補完してくれます。これがめちゃくちゃ便利で、正直これなしでは生きていけません・・・。

### Laravel(非推奨)

https://plugins.jetbrains.com/plugin/7532-laravel

よくLaravelプラグイン系でお勧めされますが、今はもう古くアップデートもされていないので微妙です。ide-helperがあれば足りてますし、他のプラグイン等でカバーできてる部分も多いので必要ないと感じています。
