---
title: "成長するためのデジタルノート術"
emoji: "💎"
type: "idea" # tech: 技術記事 / idea: アイデア
topics: ["Obsidian", "ノート", "zettelkasten"]
published: true
---

:::message alert
この記事より包括的かつ分かりやすい情報管理術をまとめている書籍が出版されているため非推奨とさせていただいています。  
↓書籍  
[Obsidianでつなげる情報管理術](https://www.amazon.co.jp/dp/B0B4K499F4)
:::

## はじめに

個人的に感じたノート術のベストプラクティスが見つかったような心持ちになったので技術共有します。

## アウトプット

### アウトプットとは？

アウトプットと一概に言っても様々な形があります。
- 紙のノートに手で書く
- インターネットを介して公開する
- 人に教える
- etc...

この記事ではアウトプットは「インターネットを介して公開する」ことをメインとして書いています。

### アウトプットのコストと利益

昨今のエンジニア界隈では必須ではないもの、アウトプットが適切に出来ているかどうかでキャリアが左右される傾向にあると感じています。

確かにアウトプットは目に見えて何をしたか（してきたか）が分かりますし、その人自身の能力を推し量るのにも利用することが出来ます。（もちろん推し量れない部分もあります）

しかし、人を判断するのに「第一印象」は重要であり、転職シーンでは密に関係すると思っています。

このアウトプットのコストと利益が焦点になります。

### アウトプットのコストと利益

アウトプットを行うとコストが発生します。

それは時間であり、お金であり、労力です。

また1度パブリックなアウトプットを行ってしまうとメンテナンスのコストも発生します。（メンテナンスが行われておらず放置されているものも多くあります）

メンテナンスのコストを0にするために、プライベートなアウトプットを行う方法もありますが、メンテナンスのコストが0になる代わりに得られるリターン（対外的な評価など）も0になってしまいます。

まとめると以下のようになります。

### 発生するcost
- 時間
- お金
- 労力
- メンテナンスコスト(パブリックにするのであれば)
- etc...

### 享受できるprofit
- 対外的な評価（パブリックな場合）
	- お金
	- キャリア
	- 地位
- 知見に対する深い理解

コストを支払うのであれば、そのコストはなるべく小さく抑え、リターンを最大にしたいのが人間の性です。


### デジタルツールによるアウトプット

自分もアウトプットに着目し、試行錯誤を繰り返してきました。

その過程でScrapBoxやNotion, Evernoteなど様々なサービスを使いつつも、イマイチしっくりくる学習術を確立することが出来ず、ナレッジが溜まっていきませんでした。

その中でもNotionは個人的に一番快適でしたが、不自由さを感じるようになりました。

最初は良かったものの、使い続けているうちにノート整理が面倒で、簡単なメモを残すには少し煩わしく感じるようになってしまいました。（あくまでノートを取るのには適していないと感じただけです。他の用途に使う分にはNotionは最高だと感じています）

そして行き着いたツールが[Obsidian](https://obsidian.md/)になります。

https://obsidian.md/

### アウトプットの工程

話が逸れましたが、つまるところアウトプットの一番の壁としては以下の工程があることだと感じています。

1. 学習する。過程でノートを取る
2. 噛み砕く
3. アウトプットとして形にする

この工程は重要で省くことは絶対にできない（してはいけない）ので変えることはしません。

しかし、この工程の中で発生する「思考・知識の整理」「知識の再検索の手間」を効率化することは出来ます。

日に日に肥大化していくノートを管理・整理するための技術としてPKMと概念があります。

## PKM

### PKMとは？

PKMはPersonal Knowledge Managementの略です。

>**Personal knowledge management** (**PKM**) is a process of collecting information that a person uses to gather, classify, store, search, retrieve and share [knowledge](https://en.wikipedia.org/wiki/Knowledge "Knowledge") in their daily activities ([Grundspenkis 2007](https://en.wikipedia.org/wiki/Personal_knowledge_management#CITEREFGrundspenkis2007)) and the way in which these processes support work activities ([Wright 2005](https://en.wikipedia.org/wiki/Personal_knowledge_management#CITEREFWright2005)).

Wikipediaより引用

DeepL翻訳

>パーソナルナレッジマネジメント（PKM）とは、人が日々の活動の中で知識を収集、分類、保存、検索、取得、共有するために使用する情報の収集プロセスであり（Grundspenkis 2007）、これらのプロセスが仕事の活動をサポートする方法である（Wright 2005）。

情報を集めるだけではなく、その集めた情報をどのように知恵へと昇華させることができるかの手法を考えるのが重要になります。

### Zettelkasten

その中でZettelkastenという手法があります。

>重要な内容を箇条書きにしたり、ハイライトの線を引いたりと、ノートの書き方は人それぞれです。**Zettelkasten(ツェッテルカステン)**と呼ばれるノート作成方法は、1冊のノートで知識を管理するのではなく、小さな紙片に1つずつ要素を書き込むことで知識を管理する方法で、紙とペン、紙を収納する箱があれば始められます。

[効率的なノートを作成できるドイツの社会学者が生み出した方法「Zettelkasten」とは？](https://gigazine.net/news/20200604-zettelkasten-note/)より引用

Zettelkastenはアウトプット障壁が低く、メモとして残したものを整理する際にさらなる理解を得ることができます。

ただZettelkastenだけでは結局ノートは肥大化してきた時に上手く管理出来ないんじゃないの？と感じてくる部分があります。

そこでLYT Frameworkというものを使用します。

## LYT Framework

[LYT Framework](https://publish.obsidian.md/lyt-kit/Umami/LYT+About)

https://publish.obsidian.md/lyt-kit/Umami/LYT+About

### LYT Frameworkとは？

[Nick Milo](https://medium.com/@nickmilo22)氏により考案されたFrameworkで

- Home Note
- Map Of Contents(以下MOC)
- Fluid Frameworks

から成り立つZettelkastenをベースに考案したPKMです。
以下は個人的にDeepL, Google翻訳で読み取った内容を個人的に噛み砕いたものです。

1次ソースをすべて理解しきっている自信がないため、1次ソースを気になった方は参照していただけると幸いです。

### LYTのメリット

LYTには以下のようなメリットがあります。

#### 信頼性

「○○完全に理解した」から「○○わからん」となる流れがありますが、その際に揺らいだ思考をLYTで構築したホームノートやMOCを使って再構築できる。

#### 柔軟性

アクセスを制限される構造（ディレクトリなど）ではなく、キュレーションするものなので、柔軟に構築しやすい。

#### 脳を活性化させる

知識の重要なカテゴリーとその重要な用語が個人に最適化されて満たされている。

#### 心理的負担の解消

デジタルノートは数が増えると構造が煩雑化し、カオスな状態になりやすいがMOCを用いることによって秩序をもたらす。

それによっていつまでも部屋が散らかっているような気分から、きれいに片付けられた部屋にいるような気分になる。

#### ノート同士の関連を促す

MOCを作ることで、ノート同士の関係性をより強固なものとし、点と点を結びやすくする。

#### 長期的な管理

予め作られたカテゴリーにノートをリンクしていくため、すべてのノートが何かと繋がっている状態になる。よって、長期的な保存と検索が可能になる。

#### 自分の未来のためになる

アウトプットを怠っていたとしても、ホームノートやMOCなどを使うことによって、すぐに作業に復帰することができる。（地図があるので作業を始めやすい）

#### 記憶力の向上

構造上ノートを開く行為を繰り返すことが多くなる。（MOCを辿ってノートを辿る）
繰り返すことによって脳に強く焼き付けられていくため、記憶に残っていく。

またコンテンツマップを作成するアクティビティを通して、自分の思考がどのように関連しているのかを真剣に考える事ができる。

空間的な地図として機能する。頭の中に空間的な地図として配置することができれば、物事を覚えやすい。

#### 満足度の向上

ノートと向き合う時間が長すぎると喜びを味わえない。LYTは色々なノートを飛び回るため、楽しさを感じる事ができる。

### コラム: ノートとアーキテクチャ

最近の話ですが、自分はPKMを知り、LYTを学んでいく上で感じたメタ認知があります。

アーキテクチャとノート管理は似ている部分が多く、結局のところ、良いアーキテクチャはメモにも通ずるところがあるということです。

たとえば、クラスを作る時のように、ノートも1つの関心事のみにとどめておくようにする方が管理がしやすいということです。

様々な関心事が集まっているノートはメスを入れにくく、修正されることがないまま、別のノートとしてほかの所でまた生まれます。

もちろん複数関心事の入ったノートを後々リファクタリングしても良いと思います。

自分が伝えたい事としては**ノート管理手法に設計技術を応用する**ことで新しい快適かつ効率もよく、生産性の高いノート術が生まれるのではないかと考えています。

LYTにおけるMOCはルーティングファイルのようなものです。

しかし、全てが応用できるわけでもなく、LYTではディレクトリによる分割を良いとは捉えていません。ディレクトリは役割が明確に線引がされる分、垣根を超えたアイデアを生み出す可能性を潰してしまうからです。

お互いに良い部分だけ掻い摘んで適用することでベストプラクティスが生まれると考えています。

自分だけのPKMを考えてみるのもまた楽しいと思います。


## LYTを実践する

### Zettelkastenをおさらい

[この記事](https://gigazine.net/news/20200604-zettelkasten-note/)からおさらいをします。

> 1. カード1枚に1アイデア
> 2. カード1枚で内容を完結させる
> 3. カードは常に他のカードとリンクさせる
> 4. カードのリンクが何を意味するのか説明する
> 5. 自分の言葉を使う
> 6. 参考文献を残す
> 7. 自分の考えを加える
> 8. 構造を気にしない
> 9. 接続カードを追加する
> 10. アウトラインカードを追加する
> 11. カードを削除しない
> 12.恐れずにカードを追加する

がルールとなっています。

これを前提にLYTフレームワークを見ていきます。

### コラム: Zettelkastenに最適なツール

Zettelkastenノートを取る際に最適のツールがあります。

そう、[Obsidian](https://obsidian.md/)です。

詳しい説明は他の記事に任せます。

- [Obsidianは最高のマークダウン『メモ』アプリである](https://pouhon.net/obsidian-introduction/5666/)
- [メモツールObsidianの使い方](https://qiita.com/koKekkoh/items/f1f684f0d7dadb658d02)

掻い摘むと、リッチなマークダウンエディタです。Wikiリンクが書きやすく、更にリンクは可視化されています。

どの情報が孤立しているのかがひと目で分かるため、Zettelkastenの「カードは常に他のカードとリンクさせる」を違反する可能性が低くなります。

また、ローカルにデータをそのまま保存をします。

プラグインも充実していて、テーマもたくさんあり、特殊な機能を使わければ無料で利用できます。(サイトとして公開やクラウドセーブを使うとなると有料)

クラウドセーブが無いと面倒な部分はありますが、MarkdownなのでGitで管理することができるため、Gitで管理することで擬似的なクラウドセーブとなっています。

面白い機能としては、検索結果のリンクをコピペして貼れるので、後述するマップオブコンテンツが作りやすいという点です。

タグで検索したり、キーワードで検索したり、情報へのアクセスが極力しやすいように作られているように感じます。

また、最初はディレクトリ構造で迷うと思うので自分の一例を掲載しておきます。

```
prefixに+,-で公開するかディレクトリか判別しやすくしてます。

.
├── + Bin // 公開サイトのAbout Me用, まだ使ってない
├── + HOME.md // ホームノート
├── + Notes // LYT(Zettelkastenノートは全部ここに)
├── + Sources // 本や記事などのリンクまとめ
├── - Private // 公開サイトで公開したくない機密情報を含むディレクトリ
├── images // 公開サイト用の画像
└── outputs // ZennやQiitaに載せる記事をストックする場所

```

自分の場合はさほどディレクトリ構造は複雑ではなく、シンプルにしています。

### ホームノートを作る

ホームノートは各ノートライブラリへの出発点となります。

LYTでは、最初は2~3個くらいのMOCを作成し、あとはノートが増えるたびに整理していこうという方針になっています。

[自分のホームノート](https://www.yum3.blog/%2B+HOME)はこのような形になっています。よければ参考にしてみてください。


### ノートを生産する

前項のZettelkastenのルールに則り、ノートをたくさん生産してください。

LYTフレームワークはノートが100個以上に膨張し始めてから効果を発揮しだすフレームワークです。

とりあえずは思考の速度を止めないようにノートをたくさん生産しましょう。

### MOCを作成する

前項を忠実に実行した場合、膨大なノートに圧倒される寸前だと思います。

では、どうするか？MOCを作る時です。

MOC(マップオブコンテンツ)とはEvergreenノートを様々な分類によってまとめたノートのことを言います。

Evergreenノートとは「その場限り」のノートとは正反対の位置にあるものであり、時間の経過と共に価値を高めて進化していくノートのことを指します。

#### Evergreenノートの特徴

- 簡潔で明確。ノートのタイトルの内容のみが含まれていて、１つのアイデアで簡潔しているアトミックなノート
- 短すぎず、長すぎず、概念を説明するのに十分な長さ
- 自分の言葉と独自の視点を使い、自分が何を言いたいのかを考え、反映したノート
- 他のノートとリンクしている
- 動的。ノートに関連する様々な出来事があるたびに、成長していく

Evergreenノートの前ステップとしてBOATノートというミニEvergreenノートも存在します。気になる人は[こちら](https://www.yum3.blog/%2B+Notes/BOAT+Notes)を参照してください。

### MOCを作成する理由

MOCは多大なメリットをもたらします。

- 関連するノートをまとめて置くことができる専用スペース
- 思考・概念・アイデアが入り交じるのでアイデア創造に最適な環境になる
- MOCを参考に記事などの成果物を作るコストが下がる
- デジタルライブラリの信頼できるナビとなる
- あるテーマについてのリマインドツールとなる
- 自分の思考が成長しても、MOCを再構築することによりノートが成長する
- MOCは流動性を維持する
- MOCは無限の柔軟性を持っているので、目次とは異なる階層を構築する
- MOCで点と点を線でつなげるため、記憶に残りやすくなる

重要な点としては「目次(Table Of Contents」とは異なる、ことです。

Table Of Contentsは明確な構造を持っています。

対して、Map Of Contentsは明確な構造を持たないため、自由は発想を行えます。

たとえば、この記事は記事なのでTOC的な構造にしています。

しかし、MOCとして作成するのであればもっと思考を凝らすことができます。

```
#### メタ概念 | 共通する概念 | ノートとプログラム設計の共通点
LYT Framework | アウトプットの利益とコスト

#### Zettelkasten | ツール
LYT Framework | Zettelkasten | Obsidian
```

のような階層的ではない自由な分類が可能となります。

このような自由な思考活動が脳を活性化させ、自分たちに思考の機会を与えてくれます。

「このアイデアとこのアイデアの関連性は・・・」と考えたり、「このアイデアとこのアイデアは対になっているから対になるように配置したり・・・」などMOCの作り方は自由です。

このアトミックなノートに対して思考するという過程が記憶に呼びかけ、理解を促進させます。

### MOCのフェーズ

#### 1. 組み立てる

ノートを全て１つのノートに放り込み、○○○MOCという名前でMOCの中に入れる

#### 2. 開発

アイデアの坩堝となった1で作ったMOCを整理する。位置関係を考えたり、互いの重要性・関係性を加味して結合組織を作成する

#### 3. 使う

自分の作ったMOCを楽しみながら使う。また、時間が経ったあとにまた見てみて、「やっぱりここはこっちだな」と思うものを移動させるなどの成長を促す。


### ノートを書くコツ

#### タグを使い分ける

ノートを検索する手法として単語検索でも良いですが、スピーディに見つける為にタグを有効活用すると良いと思います。

ただ、「このノートはどれにも属するから・・・」みたいにタグを付けることに気を取られてしまうとノートを書くストレスになります。

Obsidian的な対応としてはタグを階層にして付けるとと検索が楽になります。
`#php/laravel/pest`など

イメージとしては本来ディレクトリで分けていた分類をタグで行うことにより、検索が楽になるということです。

## まとめ

- Zettelkastenを拡張したLYT Framework
- LYT Frameworkを使ってアウトプットコストを下げる
- ZettelkastenをやるにはObsidianが使いやすい
- LYTの肝はMOC

## 参考リンク

Obsidianの使い方など

https://qiita.com/koKekkoh/items/f1f684f0d7dadb658d02

PKMとは

Reinvent Yourself with Personal Knowledge Management (PKM)

https://www.taskade.com/blog/personal-knowledge-management-pkm-guide/

LYT 参考資料

https://minerva.mamansoft.net/%F0%9F%91%A9%E2%80%8D%F0%9F%8F%ABPresentations/%F0%9F%91%A9%E2%80%8D%F0%9F%8F%AB%E3%81%A7%E3%81%8D%E3%82%8B%EF%BC%81LYT

元ソース (LYT)

https://notes.linkingyourthinking.com/Umami/The+forest+entrance

