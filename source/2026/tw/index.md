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

## カンファレンス1日目

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

* トーク概要：<https://tw.pycon.org/2026/en-us/conference/keynote/37>
* スピーカー：Tian Gao

最初のキーノートはTian Gao氏によるものです。
スライドは英語ですが発表は中国語です。

```{figure} images/tian.jpg
:width: 400

Tian Gao氏
```

トークの前半はTain氏がCPythonのコア開発者になるまでの話です。
[pdb](https://docs.python.org/ja/3/library/pdb.html)を使用しているときに、`ll`コマンドを実行するとローカルの変数の値が書きかわるというバグに遭遇しました。
これは`f_locals`という辞書の中身が上書きされるためであり、CPythonに対しての初めてのプルリクエストとして、この問題に対処する修正を2023年2月に作成したとのことです。
翌月にマージされ、オープンソースへの貢献のきっかけとなったそうです。

その後も継続的にPRを出していると、コア開発者のBrandt Bucher氏が連絡をくれて、レビューやマージを手伝ってくれるようになったそうです（Brandt Bucker氏は構造的パターンマッチの作者として有名です）。

* [Python 3.10の新機能：構造化パターンマッチング | gihyo.jp](https://gihyo.jp/article/2022/07/monthly-python-2207)
* [Pythonの構造的パターンマッチングのさらに便利なパターン紹介 | gihyo.jp](https://gihyo.jp/article/2024/01/monthly-python-2401)

そしてBrandt氏からの推薦で2026年5月からCPythonのトリアージャー（Issueの分類、管理担当）となったそうです。

その後Tian氏は「コア開発者になりたい」という目標をBrandt氏に伝え、Brandt氏からは以下の5つのステップがおすすめされました。

1. 貢献を続ける
2. Issueへの返事や、他の人のコードをレビューする
3. 特定のコンポーネントのメンテナンスを主導する
4. PEPや大きめの機能に取り組む
5. 対面で交流する

```{figure} images/5steps.jpg
:width: 400

コア開発者になるための5つのステップ
```

その後、多数のバグ修正とPRレビュー、PEP 667[^pep667]の執筆と実装、PyCon USやLanguage Summitでの発表[^pyconus-talk]や交流を行い、2024年6月にCPythonのコア開発者となったそうです。
そのときの推薦者もBrandt氏[^promote-tian]でした。

[^pep667]: [PEP 667 – Consistent views of namespaces | peps.python.org](https://peps.python.org/pep-0667/)
[^promote-tian]: [Vote to promote Tian Gao - Committers - Discussions on Python.org](https://discuss.python.org/t/vote-to-promote-tian-gao/53895)
[^pyconus-talk]: [The chaotic locals() and how we fixed it - Tian Gao - YouTube](https://www.youtube.com/watch?v=dGNt88HMUpg)

Tian氏はその後も主にpdbに関する貢献を続けており、Python 3.14でのpdb内でのシンタックスハイライト[^tian-314]、3.15でpdb内のPyREPLでの複数行の修正対応[^tian-315]、デバッグ時のオーバーヘッドを削減する最適化などを行ってきたそうです。

[^tian-315]: [What’s new in Python 3.15 — Python 3.15.1 documentation](https://docs.python.org/3/whatsnew/3.15.html#pdb)
[^tian-314]: [What’s new in Python 3.14 — Python 3.15.1 documentation](https://docs.python.org/3/whatsnew/3.14.html#pdb)

トークの後半はDatabricksへの入社とPySparkへの貢献です。
CPythonのコア開発者としての実績が評価され、Tian氏はDatabricksにPythonの専門家として採用され、PySparkの担当となりました。
しかし当初はSparkのことは全く知りません。
まずはBlackとFlake8をruffに変更したり、mypyによる型チェックの基盤の再構築、さまざまな箇所に記述してある依存情報をpyproject.tomlに統一など、コードの整理から行ったそうです。
また、CIの設定ファイルを整理したり、不安定なテストを修正、CI全体の実行時間の短縮なども行ったそうです。

その後PySparkがSparkとやりとりするUDF通信プロトコルを再設計し、拡張性の高いものとなったそうです。

このようにさまざまな貢献を行い、参画から7カ月たった2026年5月28日にPySparkのコミッターとなったそうです。7カ月間に219件のコミットを行ったそうです。

このように特定の分野に対して継続的に貢献することによって、CPythonとPySparkでのコア開発者となるという道が紹介されました。

Tian Gao氏とは今回初めて会うことができました。
継続的に着実に貢献を行っていて、頭が下がるなと思いました。

### From PyCon APAC to PythonAsia

* トーク概要：<https://tw.pycon.org/2026/en-us/conference/talk/373>
* スピーカー：Freilla Mae Espinola

このトークではPython Asia Organization（PAO）[^pao]のExecutive DirectorであるFreilla氏から、PyCon APACからPythonAsiaに変わっていったのか、について背景や課題、現状について共有されました。

[^pao]: [Python Asia - Strengthening Python Communities Across Asia](https://pythonasia.org/)

```{figure} images/freilla.jpg
:width: 400

Freilla Mae Espinola氏
```

アジア全体でのPythonカンファレンスとしては以前は「PyCon APAC」があり、2010年のシンガポールからはじまり、日本、台湾、韓国、マレーシア、タイ、インドネシアと各国持ち回りで開催され、2025年のフィリピンで終了となりました。

アジア各国にはたくさんのPythonコミュニティがあり、PyCon APACは各ローカルのコミュニティに依存し、それぞれゼロからイベントを構築していました。
そのため、ノウハウが蓄積できないという問題がありました。

この課題を解決するために2024年にPAOを立ち上げ、2026年から新しいカンファレンス（PythonAsia）を開催することとしました。
EuroPythonを主催しているEuroPython Sciety[^eps]が存在しており、この団体と同じイメージとのことです。
PythonAsiaの開催はローカルのコミュニティがリードし、PAOがサポートするという体制で運営するとのことです。

[^eps]: <https://www.europython-society.org/>

具体的な取り組みとして、イベント運営のノウハウをまとめた**プレイブック**を作成中とのことです。
他には前年のChairが次の年のChairのメンターとなり、経験を継承するそうです。
また、PythonAsia以外に以下の3つの交流プログラムを行っていくとのことです。

* Python Across Asia：Youtubeでの対談（[Python Across Asia | Episode 01 - YouTube](https://www.youtube.com/watch?v=f8omlQ8ZSis)）
* Online Charity Talks：オンラインのチャリティトークイベント（[PAO Online Charity Talks H2 2025 - YouTube](https://www.youtube.com/watch?v=OXUJhvl2m7A)）
* PAO Post：カンファレンスの記念絵はがきを送る

質問で「どのイベントが一番エキサイトしますか？」という質問には「2027年のシンガポールでのPythonAsia」との回答がありました。
筆者も参加したいなと思っています。来年が楽しみです。

### Getting Started with Signal Processing in Python: Visualizing Sound with Spectrograms

* トーク概要：<https://tw.pycon.org/2026/en-us/conference/talk/374>
* スピーカー：wat

```{figure} images/wat.jpg
:width: 400

wat氏
```

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

* トーク概要：<https://tw.pycon.org/2026/en-us/conference/talk/377>
* スピーカー：Chieh-Hung (Jeff) Cheng

```{figure} images/jeff.jpg
:width: 400

Chieh-Hung (Jeff) Cheng氏
```

KangaCode（[www.kangacode.ai](https://www.kangacode.ai/)）という子どもがPythonを学ぶプラットフォームの紹介です。
スピーカーはこのプロダクトの共同創業者です。

似たプロダクトにScratchがありますが、Scratchはプログラミング言語ではありません。
従来のPythonの学習は抽象度が高く、挫折しやすい課題があります。
9歳の子どもはエディターの画面を2分で閉じます。

そんな子どもでも楽しくプログラミングを学べるようにするために、RPGを題材にし、キャラクターの移動や探索などをPythonのコードで行います。

面白い例として「5行以内で解く」という例で、教えられていないセミコロン（`;`）を使用し、複数行のPythonコードを1行にまとめて解いた子どもがいたそうです（すごい）。

英語と台湾語のみですが興味のある方はぜひ試してみてください。

### Lightning Talks

PyCon Taiwanのライトニングトークは当日に申し込みを行い、その中から選ばれたトークが発表対象となります。
発表時間は**3分**ととても短いのが特徴です。
筆者も申し込んだところ選ばれたので、無事にイベントに爪痕を残すことができました。

タイトルは「Talks, Beer & Python: My Overseas PyCon Journey」で、自身の海外PyConに参加した経験を共有しました。
そして、得られるものがあるのでみんなも海外PyConに参加しましょう！！という内容です。
トークの最初で「海外PyConに参加したことある人？」と質問すると30%くらいの人が手を上げており、思ったよりも多くてびっくりしました。

このトークを聞いて、初めての海外PyConに参加した人と、いつかどこかで会えるといいなと思います。

* [Talks, Beer & Python: My Overseas PyCon Journeyのスライド](https://slides.takanory.net/slides/20261017pycontw-lt)

```{figure} images/lt-takanory.jpg
:width: 400

筆者のライトニングトーク
```

他のライトニングトークでは、韓国から参加しているHan Lee氏が、Pythonコミュニティによって自分が成長した体験を共有してくれました。
似たような内容をPyCon JPでも発表してくれていて、台湾はその短縮版のような感じでした。

```{figure} images/lt-han.jpg
:width: 400

Han Lee氏
```

### PyNight→ビール→夜市→ビール

カンファンス1日目が終わった後はPyNightというイベントが開催されました。
PyNightはピザなどを食べながら参加者同士で交流するイベントです。
筆者も同じテーブルになった人と自己紹介をして交流しました。

```{figure} images/pynight.jpg
:width: 250

PyNightのピザ
```

ただ、今年は会場の都合でアルコールが出せないとのことで、筆者やUKから参加しているCheukさんは「ビールが飲みたい！！」 と強く思いました。
昨日一緒に飲んでいたYuchenやKenjiに「どこかおすすめのお店ある？」と相談し、教えてもらった[Beer Geek](https://www.instagram.com/beergeektaipei/)というお店に飲みに行きました。

```{figure} images/beergeek.jpg
:width: 400

Beer Geekにて（wat、Toomas、Petertc、Soojin、Cheuk、筆者）
```

その後、臨江街観光夜市をぶらぶらし、Cheukさんがおすすめする「御品元冰火湯圓」というかき氷の店に行きました。
あとで調べたところ、ミシュラン・ビブグルマンにも載ったことがある人気店のようです。
冷たい氷の上に温かい団子が乗っているという、変わったかき氷ですがおいしかったです。

```{figure} images/ice.jpg
:width: 250

お団子の乗ったかき氷
```

その後昨日と同じ店（Flow Brewing）で一杯飲んでPyCon Taiwanの1日目が終わりました。

## カンファレンス2日目

カンファレンス2日目です。

### Keynote: From Data Collection to Skill Training: Next-Generation Sports Technology Combining AI and VR

* トーク概要：<https://tw.pycon.org/2026/en-us/conference/keynote/38>
* スピーカー：Anita Hu

```{figure} images/anita.jpg
:width: 400

Anita Hu氏
```

2日目のキーノートは台湾の精華大学の教授であるAnita Hu氏によるトークです（精華大学と書いてあって中国の大学だと思っていましたが、台湾にも同じ名前の大学があるようです）。
Anita氏はスポーツ分析向けのAI技術の会社の共同創業者でもあり、今回のトークではAIによるスポーツ分析のさまざまな事例が、さまざまなデモの動画とあわせて述べられました。

従来のデータ収集方法は多数のカメラ、GPSなどが必要で非常に高額です。
AIを活用して少ない台数のカメラ映像から、選手やボールを自動追跡したり、得点が入ったといったイベントを自動検知する仕組みを構築しているそうです。

1つのカメラ映像から、複数の人を判別して追跡するためにさまざまなAIのモデルを使用しているそうです。例えば以下の様なモデルです。

* 選手やボールなどの動態を追跡するモデル
* 試合中に発生する得点などのイベントを検出するモデル
* 追跡したトラッキングデータをもとに、チームの戦術を分析するモデル
* トラッキングデータを元に3Dで再構成するモデル

バスケットの試合を例にしていますが、たとえばバスケットの[3秒ルール](https://ja.wikipedia.org/wiki/3%E7%A7%92%E3%83%AB%E3%83%BC%E3%83%AB)では、どの選手が3秒間ペイントエリアにとどまっているかを検知します。
他にもシュートをカウントするモデルでは、2点か3点かを自動で判別します。

アマチュアの試合も対象としているので、フロアにさまざまなスポーツのラインがひかれている場合があります。
その場合でも、正しくバスケットのラインを判別するモデルがあるそうです。

他にボクシングなどのカメラ映像では人が重なっているため、見えない人の姿勢を推定するモデルや、スポーツの試合で自動追尾を行うカメラを操作するモデルなども紹介されました。
このAIが撮影した映像と人が撮影した映像を確認してもらったところ、すでにどちらが撮影したかほぼわからない状態になっているそうです。

学習データとしては、現実の試合ではほぼ発生しないシチュエーションも用意する必要があります。
そのため、シミュレーターで学習データを作成するということを行っているそうです。
学生にサッカーゲームやバスケットのゲームをプレイしてもらい、その映像を学習データとして活用しているそうです。

他にもさまざまな事例が紹介されていました。
スポーツという身近な分野に、さまざまな方向性からAIを活用した改善、効率化などが行われていることを知ることができました。
ただ、逆にそれらのことが行えている人間の審判ってすごいんだな、ということも感じました。
  
### Learn Japanese with Manga! Building a Multimodal Search Engine with Gemini Embedding 2

* トーク概要：<https://tw.pycon.org/2026/en-us/conference/talk/378>
* スピーカー：@x0mg
* スライド：<https://github.com/jeff14994/manga-lingo/blob/main/presentation/pycon2026.pdf>

```{figure} images/x0mg.jpg
:width: 400

@x0mg氏
```

日本語の学習をするときに、マンガのセリフとその音声をセットで学習したいというモチベーションで開発しているシステムの話です。
マンガで任意のセリフで検索を行うと、対応するアニメのシーンが検索され、その音声を聞くことができるというもです。

マルチモーダル検索によりテキスト、音声、動画でも近いベク取りのものが選ばれます。
ベクトル化にはGemini Embedding 2を使用したそうです。
動画を15秒単位の短いものに分割し検索対象とします。
結果として、マンガの画像から対応する動画を探すのは精度が高く、他にも音から動画を探したり、セリフからマンガと動画を探すといったことができるそうです。

ソースコードなどは以下で公開されています。
興味のある方は見てみてください。

* <https://github.com/jeff14994/manga-lingo>

### Avoiding Zero-Trade Policies in RL with a Decoupled MLOps Architecture

* トーク概要：<https://tw.pycon.org/2026/en-us/conference/talk/386>
* スピーカー：Sho Tanaka

```{figure} images/tsho.jpg
:width: 400

Sho Tanaka氏
```

日本から参加したSho Tanaka氏のトークです。
円とアメリカドルのやりとりをDQNという強化学習で実施するという実験を行った話です。
2025年の一年間の為替のデータを用意し、前半70%を学習データ、残りの30%をテストデータとして実施したそうです。
すると、取引コストなどを避けるために、最終的に「取引を一切しない」という状態になったそうです。

強化学習モデルとPythonによる実行エンジンを分離することによって、売買を行うようになったとのことです。
ただ、最終成果としては少しのマイナスだったそうです。

この内容を聞いて、やはり長期保有が一番なのか、と本題とは違うところに感想を持ちました。

### How Static Type Checkers Understand Dynamic Python

* トーク概要：<https://tw.pycon.org/2026/en-us/conference/sponsored/21>
* スピーカー：Rebecca Chen

```{figure} images/rebecca.jpg
:width: 400

Rebecca Chen氏
```

MetaのエンジニアであるRebecca Chen氏によるトークです。
Metaでは[Pyrefly](https://pyrefly.org/)という型チェッカーを作成しており、型チェッカー全般の話とPyreflyとMypyの比較などが語られました。

Metaが行ったアンケート[^survey]によると85%の人が常に、またはたまに型ヒントを使っているそうです。

[^survey]: [Python Typing Survey 2025: Code Quality and Flexibility As Top Reasons for Typing Adoption - Engineering at Meta](https://engineering.fb.com/2025/12/22/developer-tools/python-typing-survey-2025-code-quality-flexibility-typing-adoption/)

PydanticやDjangoなどのモデルで型チェックを行いたいが、型情報が存在しないためチェックできない課題がありました。
そこでPEP 681が提案され、typingモジュールに`@dataclass_transform`デコレーターが追加されました。
このデコレーターを使用することによって、データクラスに似たモデルにも、データクラスのような型情報付けて、静的型チェックができるようになります。

* [PEP 681 – Data Class Transforms | peps.python.org](https://peps.python.org/pep-0681/)

トークの後半ではPyreflyとMypyの比較がされました。
Pyreflyはさまざまな機能が組み込まれていますが、Mypyではプラグイン方式をとっています。
組み込みは使いやすく、プラグイン方式は柔軟です。

Pyreflyはまだ使ったことがありません。
組み込み型というメリットもあるので、ちょっと使ってみてもよいかなと思いました。

### お弁当とおやつ

カンファレンス中は昼にお弁当形式でのランチ、夕方にはおやつが提供されます。
また、カンファレンス2日目は暑かったので、冷たいコーヒーと紅茶も提供されていました。

```{figure} images/snacks.jpg
:width: 400

おやつ
```

### Lightning Talks

2日目のライトニングからいくつか紹介します。

インドネシアから参加しているNizar氏は、台湾他海外PyConに参加した経験について語っていました。

```{figure} images/nizar.jpg
:width: 400

Nizar氏
```

同じくインドネシアから参加しているLufti氏は、自身が主催しているPyJogja（ジョグジャカルタ）が10年間で45回のイベントを開催してきたこと、12月にミニカンファレンスを開催することが述べられました。
ジョグジャカルタはPyCon APAC 2024[^apac2024]の会場でもあり、また行ってみたい場所です。

```{figure} images/lufti.jpg
:width: 400

Lufti氏
```

[^apac2024]: [PyCon APAC 2024参加レポート | gihyo.jp](https://gihyo.jp/article/2024/11/pycon-apac-2024)

TP氏からは、AIを使わないシンプルなスライドで発表しよう！！というトークがされました。
とくにライトニングトークはシンプルな方がわかりやすいので、筆者も同感です。

```{figure} images/tp.jpg
:width: 400

TP氏
```


### Closing

Closingでは抽選会が行われました。
1日目にライトニングトークをしたHan Lee氏が当選してたんですが、もらったソフトウェアは台湾でしか動かないものだそうです（このあとのPartyで本人から聞きました）。

```{figure} images/prize.jpg
:width: 400

商品を受け取るHan Lee氏
```

参加者数は296名、72名の海外からの参加者（多い！）。全体の48%が初参加とのことです。
国別の参加者数では、韓国からが19名でダントツでした。
日本からは11名が参加したようです。私が出会えていない日本からの参加者が他にもいそうです。

```{figure} images/international.jpg
:width: 400

国別の参加者数
```

クロージングでPyNightを紹介する写真が表示されました。
このテーブルに私も座っていたんですが、このときはちょうど写真の左上でYuchenとKenjiに次に行くクラフトビールの店を相談しているところでした。

```{figure} images/closing-pynight.jpg
:width: 400

PyNightを紹介する写真
```

こうしてPyCon Taiwan 2026は無事に（カンファレンスは）終了しました。

```{figure} images/pycontaiwan2027.jpg
:width: 400

See you at PyCon TW 2027!
```

### 打ち上げに参加

イベント終了後はChairのRex氏に声をかけてもらい、台湾スタッフの打ち上げ[^pinxian]に混ぜてもらいました。
奥のテーブルでは酒好きのRex氏とYuchen氏が率先してまわりを煽り、台湾ビールを飲みまくっていました（危険なテーブルです）。

打ち上げの途中で、この日が誕生日のメンバーを祝うというサプライズがありました。ほっこりしますね。

```{figure} images/birthday.jpg
:width: 400

誕生日を祝われるメンバー（左）
```

[^pinxian]: [Pin Xian Seafood Restaurant - Google マップ](https://maps.app.goo.gl/Vongj11BabS8pqff9)

その語[Gravity](https://maps.app.goo.gl/QBiV8SrU6ykRwxzL8)というクラフトビールを扱っている店にいきました。
この店ではなんだかんだで午前2時くらいまで飲みながらいろんな話をしました。

```{figure} images/drunkers.jpg
:width: 400

最後まで残っていた酔っ払い達
```

## 非公式スプリント

次の日はPyCon Taiwanとしては本来なにもないのですが、台湾メンバーのWeiとTPが非公式スプリント（開発イベント）を開催してくれました。
この日は月曜日で、筆者はもともと仕事をする予定だったので、スプリント会場で仕事をしていました。

```{figure} images/sprints.jpg
:width: 400

非公式スプリント
```

ランチはみんなで[芝鄉涼麵](https://maps.app.goo.gl/K9s7A9AbsrF4kuHK8)というお店へ。
私は鶏肉の入った涼麵と味噌スープを注文。涼麵は冷やし中華に似た感じ、味噌スープは日本の味噌汁よりは薄味ですがどちらもおいしかったです。
こういうのは地元の人に連れて行ってもらうと、よいお店に連れて行ってもらえるのでありがたいです。

```{figure} images/noodle.jpg
:width: 400

スプリントのランチ（140台湾ドル）
```

スプリント終了後は仕事していた台湾メンバーや、観光をしていた韓国メンバーなども合流してみんなで中華料理を食べに行きました。
北京ダックを筆頭に、いろいろおいしかったです。

```{figure} images/chinese.jpg
:width: 400

円卓で中華料理
```



