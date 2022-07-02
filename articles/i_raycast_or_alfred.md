---
title: "ランチャーアプリ「Raycast」とおすすめ拡張機能"
emoji: "⚡"
type: "idea" # tech: 技術記事 / idea: アイデア
topics: ["Raycast"]
published: true
---

## Raycast

https://www.raycast.com/

### Raycastとは？

**生産性を向上させるランチャーアプリです。**

[Alfred](https://www.alfredapp.com/)をご存知の方であれば、すぐにメリットを理解できると思います。

https://www.alfredapp.com/

RaycastはAlfredと同等のことを行い、機能拡張が簡単にできます。

具体的に何ができるのでしょうか？それを説明していきたいと思います。

### Raycastのここが良い!　〜基本編〜

#### 使うアプリを即時に起動

ホットキーを押して、Raycastウィンドウを出してアプリ名を入れるだけで即時に開く・移動ができます。

仮想デスクトップが多い方にはとっても役立ちそうですよね？

#### かゆいところに手が届く

コピーしてペースト、コピーしてペースト、コピーしてペースト・・・何度も同じ作業を繰り返していませんか？

Raycastにあるクリップボード履歴から呼び出す機能を使えば何度もコピーする必要はありません！

更にクリップボードからスニペット登録ができたり、画像コピーも残っていたり、カラーコードは別形式に変換などもできます。

詳しくはこちらを参照してください。

https://dev.classmethod.jp/articles/eetann-used-raycast/

また、ちょっとしたメモを取っておきたいけど・・・という時にはフローティングメモがオススメです。

他にもウィンドウのサイズを簡単に変えられたり、よく使う単語を登録しておいたり、今日の予定を確認したり、電卓代わりにも使えます！

「もっと他のこともしたい・・・」と感じた方は、スクリプトを実行できるのでShellScriptやAppleScriptを書くことで更にできることは増えます！

公式のスクリプト置き場もあります。

https://github.com/raycast/script-commands/tree/50dd2d231f4ef53d4e12c5291b6a12181e357441/commands

またComand + K でアクション選択を行なうこともできます。

例えばカレンダーアプリでMeetのURLが設定されている場合は、RaycastからMeetに参加することも可能です。

****


####  コラム: Alfredと何が違うの？

公式の方のFAQでも回答があり、拡張機能が強いとあります。

https://www.raycast.com/faq

##### UI/UXが良い

AlfredはやはりUIが少し一世代前のように見えてしまうため、少し直感的でない部分があったり、「この機能はどう使えばいいんだ？」という難しさがあります。

それに比べてRaycastは直感的に設定が行えるため導入しやすいというメリットがあるように感じています。

##### 拡張機能追加が無料でできる

Alfredにも拡張機能と似たようなWorkflowという機能があります。

しかし、Workflowは課金が必要です。シングルライセンスが34ユーロ、生涯ライセンスが59ユーロとなります。日本円で4700円程度と、8300円程度になります。

AlfredのWorkflowのほうができる幅が広いのは確かですが、なかなか踏み出せない人にとってRaycastは最高の選択になります。

拡張機能自体もReactで書くことができるため、Reactに馴染みがある人は手間には感じないでしょう。

基本機能でAlfredでは有料でないと使えない機能も使えるのが魅力的です。

##### その他

巨人の肩をお借りします。以下の記事が参考になります。

https://blog.kyanny.me/entry/2021/12/22/221925

https://motemen.hatenablog.com/entry/2022/02/raycast?utm_source=pocket_mylist

https://uit-inside.linecorp.com/episode/114

---

### Raycastのここが良い!　〜応用編〜

Raycastの特徴としてはやっぱり**拡張機能**を追加できることです。

有料版AlfredにもWorkflowという拡張機能と似たようなものです。

ここからはオススメの拡張機能を紹介します。

#### ランダムなデータを生成する

Fakerのような機能を提供してくれる拡張機能です。

頻繁に使うか？と聞かれてしまうと微妙なところですが、hogehogeの代わりに使ってみてはいかがでしょうか？

https://www.raycast.com/loris/random

#### GoogleChromeの履歴やタブを操作する

Chromeで現在開いているタブや、履歴を検索できます。

また、タブを新規作成するコマンドの方では、最近閉じたタブを過去20個くらいまでは履歴を持ってきてくれます。

https://www.raycast.com/Codely/google-chrome

#### GoogleChromeのプロファイルごとに操作する

Chromeで複数のアカウントでログインしている時、入れ替えが少し面倒です。

その面倒を限りなく楽にするためにこのプラグインは使用できます。

https://www.raycast.com/frouo/google-chrome-profiles

#### homebrewを操作する

Brewでインストールされているものや、パッケージ、アップグレードなどをRaycastで行えます。パッと「あれあるのかな？」という時に便利です。

https://www.raycast.com/nhojb/brew

#### プロセスをKillする

強制終了したいアプリがある時、ターミナルからキルするかアクティビティモニタから強制終了するのが普通ですが、この拡張機能でRaycast上から行なうことができます。

https://www.raycast.com/rolandleth/kill-process

#### Githubを操作する

Issueの作成やPR作成、またPR表示やワークフローの実行、リポジトリの検索などをRaycastで行えます。

https://www.raycast.com/raycast/github

#### SpeedTestする

サクッとお使いのネット回線速度を調べられます。

https://www.raycast.com/tonka3000/speedtest

#### GoogleDrive検索する

Google Drive上の全件検索をRaycastで行えます。

https://www.raycast.com/vishaltelangre/google-drive

#### Jiraを操作する

Jiraユーザー向けになりますが、Githubのと同様、Jiraの操作もRaycastで行えます。

https://www.raycast.com/raycast/jira

#### Confluenceを検索する

Confluence Wiki上の検索をRaycastで行えます。

https://www.raycast.com/daviddkkim/confluence-search

#### Bitbucket操作する

Bitbucket上のリポジトリ検索や自分のプルリクエストを確認することができます。

https://www.raycast.com/Francois/bitbucket

#### チートシートを確認する

CheatSheetsを検索し、Raycastに表示することができます。

https://www.raycast.com/destiner/cheatsheets

#### VSCodeで最近開いたプロジェクトから開く

VSCode側にも

https://marketplace.visualstudio.com/items?itemName=alefragnani.project-manager

の拡張機能が必要になりますが、最近開いたプロジェクトから順番に見られて開くことができます。

https://www.raycast.com/thomas/visual-studio-code

#### Dockerの状態を確認する

Dockerのコンテナを起動・停止することができたり、ディレクトリ関係なしにDocker composeプロジェクトを確認でき、コンテナを停止・起動することができます。

Imageの確認もでき、Imageの削除もできます。

https://www.raycast.com/priithaamer/docker

#### Json をフォーマットする

Jsonをフォーマットする拡張機能です。ただそれだけ。

https://www.raycast.com/destiner/json-format

#### Notionを検索する

Notionのデータを検索することができます。

Notionを使ってると割と検索の存在を忘れてしまうので良いかもしれません。

https://www.raycast.com/reckoning-dev/search-notion

#### Slackのステータスを設定する

SlackのステータスをRaycastで簡単に設定することができます。

https://www.raycast.com/petr/slack-status

#### JetBrains製品の最近起動したプロジェクトから開く

JetBrains製品のIDEで開いた最近のプロジェクトから開くことができます。

プロジェクトが溜まってきたり、IDEをいろいろまたがってると面倒なのでありがたいです。

https://www.raycast.com/gdsmith/jetbrains

#### npm Packageを検索する

npm packageを検索でき、READMEを読むことやnpm, yarn, pnpmに対応したインストールコマンドをコピーすることができます。パッケージネームをコピーすることもできます。

もちろんそのままGithubに飛ぶことも可能です。

https://www.raycast.com/mrmartineau/search-npm

#### stackoverflowを検索する

Stackoverflowをraycast上で検索ができます

https://www.raycast.com/reckoning-dev/stackoverflow

#### .gitでリポジトリを一覧表示する

ローカルの.gitを参照してリポジトリ一覧表示ができます。

そのままVSCodeを開いたり、originに飛ぶことができるので便利です。

https://www.raycast.com/moored/git-repos

#### XCodeを操作する

XCodeの操作をraycast上で行なうことができます。

https://www.raycast.com/SvenTiigi/xcode

#### awsを操作する

ec2, sqs, codePipelines, console, CloudFormation, DynamoDBをRaycastから一覧表示することができ、そのままジャンプできます。

https://www.raycast.com/Falcon/aws

#### Portを操作できる

ポートを使用しているプロセスを終了させ、即時に開放することができます。

https://www.raycast.com/lucaschultz/port-manager


## まとめ

- Alfred課金ユーザーはAlfred, Raycastどちらでも良い
	- Alfred 5で自動化機能がやりやすくなるのでメインRaycast, 自動化Alfredというのも手
- お金をかけたくないユーザーにはRaycastは最高の選択になるかもしれない
- RaycastはTypeScript/Reactで拡張機能が作れるので、自分で拡張機能を作る楽しさもある