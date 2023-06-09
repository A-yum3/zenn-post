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

他にもProgressBarを置き換えるプラグインはたくさんあるので、好きなものを使ってください。

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

DocBlocksをサポートしてくれます。

###  Php Inspections (EA Extended)

https://plugins.jetbrains.com/plugin/7622-php-inspections-ea-extended-

PHPを書く上で、バグを引き起こすかもしれない部分に警告文を出してくれます。

PHPStanとはまた草分けが違い、if文で「この条件おかしくない？」とか「emptyでいいの？nullのがよくない？」みたいな助言をしてくれます。

インスペクションでサクッと適切な形に自動整形してくれるので便利で手放せません。

また、アーキテクチャの問題や弱い方やパフォーマンス、セキュリティ問題など幅広い中でアラートを早めに出してくれます。

1行関数をArrow Functionに変えるのも簡単に整形してくれるので楽です。
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

### Gitmoji Plus: Commit Button

https://plugins.jetbrains.com/plugin/12383-gitmoji-plus-commit-button

GitmojiをPhpStorm上のGitHubクライアントから簡単に使えるようにするプラグインです。

Gitmojiだと絵文字で何をしたコミットの種類なのかがひと目でわかるため、便利です。

###  Tabnine AI Code Completion- JS Java Python TS Rust Go PHP & More

https://plugins.jetbrains.com/plugin/12798-tabnine-ai-code-completion-js-java-python-ts-rust-go-php--more


Tabnineはタブ補完で予測を出してくれる上に、ファイル上からも予測を行なってくれます。似たような文が続くテストコード等では大活躍で、少し癖はあるものの、効率は大幅に向上します。ぜひ利用して欲しいプラグインです。

Tabnineはかなり重宝しています。
補完が効かない場所もAIによって補完を出してくれる場合があったり、連想配列のkeyもサクッと予測してくれるのでかなり便利です。

統計も出るので、どれくらい自動化されたのかが分かりやすいです。
自分は15%くらいです。

###  Translation

https://plugins.jetbrains.com/plugin/8579-translation

Google翻訳を楽に行えます。

本領発揮をするのは**メソッドとかにカーソルを置いてると出てくるポップアップとかにも簡単に翻訳を掛けられることです。**

ライブラリのコメントは英語で書かれていることが多いので、重宝します。

### Inspection Lens

https://plugins.jetbrains.com/plugin/19678-inspection-lens

コードに問題があるときに波線などの警告が出ると思います。その警告文に対していちいちカーソルをあわせるのは少し面倒ですよね？

そういったときに役立つプラグインがあります。それがInspection Lensです。

Inspection Lensはエラーが発生している行にエラー文を表示してくれるため、カーソルを当てる必要もなく、問題点がわかります。

ぜひ、オススメです。

### GitLink

https://plugins.jetbrains.com/plugin/8183-gitlink

コードエディターからGitHubへのリンクをコピーできたり、GitHubを開くことができます。

Slackなどで意外とコードURLを共有することはありませんか？その際にこのGitLinkを使えばスムーズにURLを見つけることができます。

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
