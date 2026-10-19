# PyCon Taiwan 2026

## PyCon Taiwan 2026とは

## Day 1

### Opening

* スポンサー、

### Keynote

* From CPython to PySpark
* pdfのバグを直した。llを実行するとローカルでの変更がかきかわる。f_locals
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

### LightningTalk

### PyNight

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

* 

### Party

