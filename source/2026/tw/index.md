# PyCon Taiwan 2026

鈴木たかのり（[@takanory](https://x.com/takanory)）です。
2026年10月に台湾の台北で開催された、プログラミング言語Pythonのカンファレンス「PyCon Taiwan 2026」に参加してきたので、その様子をレポートします。


## PyCon Taiwan 2026とは

PyCon Korea 2026のイベント概要は以下の通りです。

|項目|内容|
|--|--|
|URL|<https://2026.pycon.tw/>|
|日程| 2026年10月17日（土）、18日（日）|
|場所| 台北市 |
|会場| TODO大学名 |
|参加費| 個人：60,000 KRW（約7,000円）、Tシャツ 15,000 KRW |
|主催| TODO確認 |

```{figure} images/pycontaiwan2026.png
:width: 400

PyCon Taiwan 2026公式サイト
```

筆者がPyCon Taiwanには2024、2023、2019年など複数回参加しています。
初めて参加した海外PyConもPyCon Taiwanでした。過去のレポートは以下を参照してください。

* [PyCon Taiwan 2024レポート](https://gihyo.jp/article/2024/10/pycon-tw-2024)
* [PyCon Taiwan 2023レポート](https://gihyo.jp/article/2023/09/pycon-tw2023)
* [PyCon Taiwan 2019レポート](https://gihyo.jp/news/report/01/pycon-tw2019)

## カンファレンス前日

カンファレンス前日に台湾入りをしました。
この日はスピーカーディナーがありましたが、残念ながら私はスピーカーではないので予定がありません。
すると台湾メンバーのYuchenがクラフトビールの見学ツアー（飲み放題付き）を企画してくれました。
私は残念ながらツアーには参加できなかったんですが、飲み放題には参加し[Taiwan Head Brewers](https://headbrewers.com.tw/en/)のさまざまなビールを楽しみました。いやー、楽しかった。

```{figure} images/day0beer.jpg
:width: 400

左からGTB、Kenji、筆者、Yuchen、Rex
```

飲み放題は21時までなので、その後カンファレンス会場の近くにある[Flow Brewing](https://www.flowbrewing.beer/)に移動しました。
場所をアジアメンバーに連絡しておいたところ、スピーカーディナーや今日到着したメンバーがすでに集まっていました。
いつものPyConがスタートしたな、という感じです。

```{figure} images/day0beer2.jpg
:width: 400

アジアメンバーを中心に集合
```

## Day 1

今年のカンファレンス会場は台北医学大学（Taipei Medical University）の教育棟（Teaching Building）です（[Googleマップ](https://maps.app.goo.gl/kSNBtUQubSAQV1qn7)）。
台北101から徒歩15分くらいの場所にあります。

```{figure} images/university.jpg
:width: 400

立派な大学名
```

### Opening

カンファレンスのオープニングではConference ChairのRex氏により、イベント内容やスポンサーの紹介がありました。
私はRex氏が今年のPyCon TaiwanのChairだということを知らなかったので（主催者の一人だとは思っていましたが）、少しびっくりしました。
Chairなのにスピーカーディナーではなく、ビールツアーの方に来ていたんですね。

```{figure} images/opening.jpg
:width: 400

Conference ChairのRex氏によるオープニング
```

### Keynote: From CPython to PySpark

最初のキーノートはTian Gao氏によるものです。
スライドは英語ですが発表は中国語です。

* pdbのバグを直した。llを実行するとローカルでの変更がかきかわる。f_locals
* 中国語でのトーク
* Brandt Bucherが連絡してくれたらしい
* 2023 May 4にPython Triagerになった
* Core devへの道。Brandtのおすすめの5ステップ
* さまざまなコードを実装
* PEP 667を書いた
* PyCon US 2024で発表してLanguage Summitに参加した
* 2024 June 6にCore devになった
  * pdbのデファクトメンテナー
  * これが終わりではない
* 3.14でpdbでのシンタックスハイライト、3.15でPyREPLの複数行修正

#### Part 2: databricksに入った

* PySpark teamに入ったがSparkのことはなにも知らない
* Black Flake8をruffに変更
* 型ヒントを入れた
* dependencyがあちこちに書いてあったものをpyproject.tomlに統一
* sparkのUDFの仕組みを書き換えた
* 2026 May 28にSparkのコミッターに
  * 7カ月で219のコミット

### From PyCon APAC to PythonAsia

* Freilla
* PyCon PHの2017でボランティアに
* taiwanでは3回(2014, 15, 22)PyCon APACを開催。ただ2022はオンライン
* AsiaにはたくさんのPythonコミュニティがある
* PyCon APACの開催は各ローカルコミュニティに依存していた。ゼロから作る
* 15回 PyCon APACが開催されてきた
* PAOを2024年に立ち上げ、PythonAsiaを開催することにした
* EuroPython Scietyと同じイメージ。地域カンファレンスのsteward
* localコミュニティがリードしPAOがサポートする
* playbooksを書いているらしい→どこで見れるんだろ
* 前のchairが次のchairのメンターになる(なるほどー
* 3つのプログラム: Python Across Asia, Online Charity Talks, PAO Post
* 4つのやることあるよ
* Playbooksはどこにあるの?→ブースにQRコードあるよ
* biggest challenge→language、
* どのイベントが一番エキサイトする?→2027のシンガポール

### Getting Started with Signal Processing in Python: Visualizing Sound with Spectrograms

* wat
* 5ステップでできるようになるよ
* sounddeviceを使って録音→Numpy aarryになる
* soundfileライブラリで保存と読み込み。wavで保存される
* matplotlibで音の大きさを表示
* 短い時間を取り出してFFTで変換
* Hann windowで真ん中を強調している
* windowsの長さで結果が変わる
* githubあるよ
* 試せるWebもあるよ

````{admonition} コラム：ここにコラムタイトル入れて
watさんの発表体験のコラム
````

### Learning Python Through KangaCode

* KangaCodeのFounder
* https://www.kangacode.ai/tw
* 似たプロジェクト: Scratch
* 9さいのこどもは2分でエディターを閉じる
* RPGにする
* 5行以内でとくという問題で、セミコロンを使って3行で実行した(ウケる

### Lightning Talks

PyCon Taiwanのライトニングトークは当日に申し込みを行い、その中から選ばれたトークが発表対象となります。
時間は**3分**とさらに短いのが特徴です。
筆者も申し込み選ばれたので、無事にイベントに爪痕を残すことができました。

筆者の発表は「Talks, Beer & Python: My Overseas PyCon Journey」というタイトルで、自身の海外PyConに参加した経験を共有しました。
そして、得られるものがあるのでみんなも海外PyConに参加しましょう！！という内容です。
トークの最初で「海外PyConに参加したことある人？」と質問すると30%くらいの人が手を上げており、思ったよりも多くてびっくりしました。

このトークを聞いて海外PyConに参加した人と、いつかどこかで会えるといいなと思います。

* [Talks, Beer & Python: My Overseas PyCon Journeyのスライド](https://slides.takanory.net/slides/20261017pycontw-lt)

```{figure} images/lt-takanory.jpg
:width: 400

筆者のライトニングトーク
```

他のライトニングトークでは、韓国から参加しているHan Lee氏が自身のPythonコミュニティによって成長した体験を共有してくれました。
似たような内容をPyCon JPでも発表してくれていて、台湾はその短縮版のような感じでした。

```{figure} images/lt-han.jpg
:width: 400

Han Lee氏
```

### PyNight→ビール→夜市→ビール

カンファンス1日目が終わった後はPyNightというイベントが開催されました。
PyNightはピザなどを食べながら参加者同士で交流するイベントです。
筆者も同じテーブルになった人と自己紹介をして交流しました。

ただ、今年は会場の都合でアルコールが出せないとのことで、筆者やUKから参加しているCheukさんは「ビールが飲みたい！！」 と強く思いました。
昨日一緒に飲んでいたYuchenやKenjiに「どこかおすすめのお店ある？」と相談し、教えてもらったBeer Geekというお店に飲みに行きました。

(6人の写真)

その後、臨江街観光夜市をぶらぶらし、Cheukさんがおすすめしてくれたかき氷を食べに行きました。
冷たい氷の上に温かい団子が乗っているという、変わったかき氷ですがおいしかったです。

(かき氷の写真)

## Day 2

### Keynote

* 精華大学のPh.D
* AIでスポーツのビデオを解析
  * イベントを取り出す
  * スイングが5種類、コーチは30種類という→研究者が見分けられないのでラベルを付けられない
  * 人をトラック、ボールをトラックする
  * QRコードに参考のコードがあるよ
* センサーベースとカメラを組み合わせて選手の動きをトラックする
* 1つのカメラ映像で人をトラックするためにさまざまなモデルを使用する
  * どっちのチームの何番かを認識する
  * バスケットの3秒ルールの対象化をAIで判断する
  * バスケットのコートだが他のスポーツのラインが描いてある
* シュートをうったら点数を自動カウントする
  * 高いボールがゴールの近くを通るとシュートとカウントする
  * 2点か3点かの検出
* T1リーグと共同している
  * https://omniscores.com/
* シュート練習の内容を自動でカウントする。どの位置からだとどのくらい成功するか
* 人とAIが協力する
  * 人がタブレットで入力する
* 市場が小さい
  * Saasにした。動画をアップロードしてハイライトを作成する
* 撮影にAIのトラッキングカメラを使う
  * カメラが早く動くので情報をみのがす
  * カメラを適切に動かすAIモデルを作った
  * AIがとったか人がとったかを確認した→ほぼわからない
* シミュレーターでデータを作成する
  * 学生にゲームをプレイしてもらう
* Movement Analysis
  * 動作分析のアプリはたくさんある
* 試合中に練習でしていた動作ができるか
  * 他の人と重なっているときに後ろの人の動作がわかる。論文査読中
* 複数のカメラだとキャリブレーションが必要
  * 4代のGoProでできるようにした
* Opus 5.5, Gemini 4 Argonでいろんなことができる
  * 開発する必要あるか?
  * コストが高い→APIコストが下がったら優位性がなくなる
* スマートグラスを使って誰を見ているか
* 戦術練習でVRで人を動かす
* 野球の練習でコーチが設定した内容でボールを投げる、正確にトスする、スイングを記録する
* Q&A
  * ビジネス→B2B→B2C→B2B2C
  
### Learn Japanese with Manga! Building a Multimodal Search Engine with Gemini Embedding 2

* 1つのマンガとアニメのシーンを検索し、日本語を読んで聞くということをやりたい
* マルチモーダルで近いベクトルのものを選ばれる
* Gemini Embedding 2を使用
* 動画を15秒のchunkに分割
* 768bitでよい
* テキストマンガを探す
* 画像から対応する動画を探す→精度が高い
* 音を入力して動画を探す
* マンガのページから田動画を探す

### Avoiding Zero-Trade Policies in RL with a Decoupled MLOps Architecture

* 円とUSDのやりとりを強化学習で処理する
* 2025年の1年のデータで前半70%で学習して後半30%で実行する
* エージェントがトレードしなくなる
* 長い期間保持する方がよい→たくさんやりとりすると負ける

### How Static Type Checkers Understand Dynamic Python

* pyreflyのはなし
* 85%の人がtype hintを使っている
* dataclassのannotationをどうしるのか?
  * PEP 681: dataclass transforms
* mypyとpyreflyの比較

### Panel

Kir Chou
胡敏君, 高天, Max Lai, 陳宜昌

### LT

* Zarrというデカイデータをstrreamするもの
* Indonesiaから参加した人。たいわん他に参加しているっぽい
* PyCon Koreaの参加者からorganizerになった話
* Jogjaは10年で45イベント。12月にmini pyconを開催するとのこと
* TP: AIを使わないスライドが好きという話(わかる

### Closing

Closingでは抽選会が行われました。
1日目にライトニングトークをしたHan Lee氏が当選してたんですが、もらったソフトウェアは台湾でしか動かないものだそうです（このあとのPartyで本人から聞きました）。

(Han Leeの写真

参加者数は296名、72名の海外からの参加者（多い！）、48%が初参加とのことです。
国別の参加者数では、韓国からが19名でダントツでした。
日本からは11名が参加したとのことです。私が出会えていない日本からの参加者が他にもいそうです。

(国別参加者数

クロージングでPyNightを紹介する写真で

(PyNightを紹介する写真

### Party

