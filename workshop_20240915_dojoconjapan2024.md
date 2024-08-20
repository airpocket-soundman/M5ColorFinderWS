# M5いろさがしワークショップ
  
M5StickCを使って、色を探すゲームを制作するワークショップです。  
プログラム言語としてUIFlowというブロックプログラミングを使用します。  
対象年齢：小学4年生以上
必要機材および環境：
・プログラミング用PC
・M5StickC Plus もしくは M5StickC Plus 2
・M5Stack用カラーセンサユニット
・Wi-Fi 2.4GHz帯接続
  
# M5いろさがしとは
  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/otama.png?raw=true" width="25%" alt="otama mark">  

otomaさん制作の色探しゲーム。
二人のプレイヤーがお題で示された色に近い色を探してカラーセンサで読み取り、より近い色を探したプレイヤーが勝ち。  
参考サイト：[https://protopedia.net/prototype/5078](https://protopedia.net/prototype/5078)  

# 講師自己紹介
  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/airpocket2-removebg-preview.png?raw=true" width="20%" alt="airpokcet mark"> 山下 泰弘/airpocket  
ホビーメイカー  
M5Stack Japan Creativity Contest 2021 優勝  
M5Stack Japan Creativity Contest 2022 M5Stayle賞  
M5Stack Japan Creativity Contest 2023 準優勝  
  
# M5Stackとは
  
・M5Stackとは、主にESP32シリーズのSoCをコントローラに採用したマイコンボード。  
・メインラインの製品群は5cm各の正方形のプラスチック筐体に各種パーツを重ねる（スタックする）ことで機能拡張できる。  
・モデルによるがディスプレイ（タッチ/非タッチ）、物理ボタン、Groveコネクタポート、各種IOを搭載しているため、工作の手間を最小限に抑えてさまざまなソリューションを開発できる。  
・ESP32搭載モデルはWi-Fi/Bluetoothによる無線接続も可能。  
・単体のマイコンボードとしてだけでなく、多様なセンサ類などの追加ユニットやUIFlowというビジュアルプログラミング環境などを含めたエコシステムが最大の特徴。  
  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/M5_1.png?raw=true" alt="lineup_01"><br>  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/M5_2.png?raw=true" alt="lineup_02"><br>  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/M5_3.png?raw=true" alt="lineup_03">  
  
# スポンサー紹介
  
株式会社スイッチサイエンス様  
今回のワークショップに使用する機材をご提供いただきました。ありがとうございます。  
M5Stack製品を日本に広め各種イベントを開催。ユーザーグループの発展にも大きな協力をされておりいちユーザーとしては足を向けられません。  
M5Stack製品の在庫も充実しています。  
  
# 事前準備
  
## 充電
  
M5StickC Plus/Plus2には、リチウムイオンバッテリーが搭載されています。事前に充電することで単独で使用できます。  
USB Type Cケーブルで充電できます。  
  
※リチウムインバッテリーを搭載しているため取り扱いには注意が必要です。  
過充電、過放電、夏場の車内放置などを避け、スマホと同等の取り扱いを心がけましょう。  
  
## ファームウェア書き込み
  
M5いろさがしは「UIFlow」というブロックプログラミング環境を使用します。  
購入直後のM5Stickにはデモプログラムが書き込まれているため、「M5Burner」というツールを使ってUIFlowのファームウェアを書き込む必要があります。 

ファームウェアの書き込みはUSBケーブルを通じて行いますので、M5StickCとPCをUSBケーブルで接続したうえで以下の作業を実行してください。   
  
### M5Burnerのダウンロードと解凍
  
M5Bunerを以下のサイトからダウンロードします。  
https://docs.m5stack.com/en/download
  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/burner_download.png?raw=true" alt="burner download"><br>  
  
ダウンロードしたファイルを解凍しツールを実行します。  
  
### ファームウェアのダウンロード
  
M5Burnerを実行したら、左のカラムからコントローラの大分類を選択します。  
今回のワークショップでは①「STICKC」を選択します。  
右のカラムにはファームウェアの種類が表示されます。  
「M5StickC Plus」に「UIFlow」のファームを入れるため、「UIFlow_StickC_Plus」を選択します。  
「M5StickC Plus2」を使用する場合のファームは「UIFlow_SticC_Plus2」です。  
目的のファームウェアを見つけたら、②のバージョンを確認します。  
ファームウェアのバージョンは頻繁に更新されますが、特別な理由が無い限り最新版で問題ありません。  
続いて③「Download」ボタンをクリックすると、目的のファームウェアをPCにダウンロードできます。  
  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/firmware_download.png?raw=true" alt="firmware download"><br>  
  
### ファームウェアの書き込み
  
目的のファームウェアがダウンロード出来たらM5Stickに書き込みます。  
書き込みはUSBケーブルを通じて行いますので、PCとM5StickがUSBケーブルで接続されていることを確認してください。  
  
ファームウェアがダウンロードできていると、「burn」ボタンが表示されていますのでクリックします。  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/firmware_burn.png?raw=true" alt="firmware burn"><br>  
  
書き込み先の確認ダイアログが開きますので、M5Stickが接続されているポートを選び、「Next」ボタンをクリックします。  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/firmware_burn_2.png?raw=true" alt="firmware burn 2"><br>   
  
続いてWi-Fi接続先を問われますので、接続先のSSIDとパスワードを入力して「Next」をクリックします。  
M5Stackシリーズは原則2.4GHz帯のみ対応していますので、2.4GHz帯のアクセスポイントを指定してください。  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/firmware_burn_3.png?raw=true" alt="firmware burn 3"><br>  
  
書き込みが開始されるのでしばらく待つと以下の通り表示されると完了です。「Burn successfully, click here to return」のボタンを押して下さい。
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/firmware_burn_4.png?raw=true" alt="firmware burn 4"><br>  
  
正しく設定されている場合、M5StickCの画面い次の写真の様にAPI KEYが表示されます。  
（※API KEYは端末ごとに異なる値が自動的に設定されます。）  
API KEYが表示された場合はM5Burnerを終了してください。  
表示されない場合は設定が間違っている可能性がありますので、次項を参考に設定を見直してください。  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/api_key.png?raw=true"  width="20%" alt="api_key"><br>  
  
### ファームウェアの設定確認
  
M5Stickの設定を確認するにはM5Burnerの「Configure」ボタンを押して設定を読み込みます。  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/configure_1.png?raw=true" alt="configure 1"><br>
  
接続先のポートを入力するダイアログが表示されるので、StickCが接続されているポートを指定して「Load」ボタンをクリックしてください。  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/configure_2.png?raw=true" alt="configure 2"><br>
  
現在の設定が表示されるため、以下の項目をチェックして正しい値に変更し「Save」ボタンをクリックして書き込んでください。
  
・COM:現在接続しているポートを選択  
・Start Mode:Internet Modeを選択  
・Server:flow-jp.m5stack.com（※この項目は任意のサーバでOK）  
・WIFI SSID:2.4GHz帯のアクセスポイントを入力  
・WIFI Password:アクセスポイントのパスワードを入力  
  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/configure_3.png?raw=true" alt="configure 3"><br>
  
# M5いろあつめ　制作
## UIFlowを開く
UIFlowはブラウザ上で動作するブロックプログラミング環境です。  
次のサイトを開いてみましょう。  
https://flow.m5stack.com/  
  
### デバイスの選択
UIFlowのエディタ画面が開いたら、右上の三本線のアイコンをマウスオーバーし、「設定」をクリックしてください。  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/uiflow_00.png?raw=true" alt="uiflow_00"><br>
  
Api Keyの欄には、M5StickCのディスプレイに表示されているAPI KEYを入力します。  
Serverは任意ですが、ここでは「flow-jp.m5stack.com(Japan)」を選択します。  
下段には使用するデバイスがアイコンで表示されていますので使用するデバイスを選択します。ここではM5StickC Plusを選択しています。  
全て入力できたら「OK」をクリックします。  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/uiflow_01.png?raw=true" alt="uiflow_01"><br>
  
### カラーセンサユニットを接続する
  
M5いろあつめでは、カラーセンサユニットを使用します。M5StickCとカラーセンサを付属のGroveケーブルで接続してください。  
  
UIFlowでもセンサを追加するとセンサを制御するブロックが使える様になります。  
画面左側の「＋」アイコンをクリックして接続するUnitを選択します。  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/uiflow_02.png?raw=true" alt="uiflow_02"><br>
  
M5Stackで使えるユニットがたくさん表示されます。ダイアログ上部の検索窓に「color」と入力して絞り込みます。  
今回使用するカラーセンサのチェックボックスをクリックします。「port」にA(33,32)と表示されていることを確認して右下の「OK」をクリックしてください。  
「port」はM5Stickとセンサユニットの接続に使用するポートを指定する項目です。カラーセンサはport Aを使用します。  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/uiflow_03.png?raw=true" alt="uiflow_03"><br>
  
## M5Stickのディスプレイをデザインする
  
UIFlowの画面左のエリアで、ディスプレイのデザインができます。  
M5いろあつめでは、3つの四角形と二つのラベル（テキスト表示）を使用します。  
まず、左側にある「Rect」アイコンをM5StickCのディスプレイにドラッグします。  
ディスプレイに小さな四角が表示されるので、この四角をクリックしてプロパティを開きます。  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/uiflow_04.png?raw=true" alt="uiflow_04"><br>
  
プロパティの以下の項目を修正します。  
X:0  
y:0  
Width:135  
Height:120  
  
M5Stick C Plus及びC Plus 2のディスプレイは幅135、高さ240ピクセル、原点(0, 0)はディスプレイ左上です。
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/uiflow_05.png?raw=true" alt="uiflow_05"><br>
  
続いて残り二つの四角を引き出してディスプレイ上に適当に配置します。  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/uiflow_06.png?raw=true" alt="uiflow_06"><br>
  
それぞれrectangle1、rectangle2と命名されているので、プロパティを開いて次の通り設定します。
  
・rectangle1  
X:0  
y:122  
Width:66  
Height:90  

・rectangle2  
X:69  
y:122  
Width:66  
Height:90  

<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/uiflow_07.png?raw=true" alt="uiflow_07"><br>
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/uiflow_08.png?raw=true" alt="uiflow_08"><br>
  
続いて、テキストを表示するための「ラベル」を配置します。  
左端のLabelアイコンをディスプレイ上に二つドラッグします。それぞれ「label0」「label1」と表示されていればOKです。  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/uiflow_09.png?raw=true" alt="uiflow_09"><br>

## 変数を作成する
  
プログラムで使用する変数を作成します。  
ブロックのリストから「変数」＞「変数の作成…」をクリックすると変数を作成できます。  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/uiflow_10.png?raw=true" alt="uiflow_10"><br>
  
作成する変数名を入力して「OK」をクリックします。
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/uiflow_11.png?raw=true" alt="uiflow_11"><br>
  
同様に以下のすべての変数を作成してください。  
・distance1  
・distance2  
・player1_b  
・player1_g  
・player1_r  
・player2_b  
・player2_g  
・player2_r  
・step_number  
・target_b  
・target_g
・target_r  

<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/uiflow_12.png?raw=true" alt="uiflow_12"><br>
  
作成した変数のうち、「step_number」を初期化します。  
「変数」ブロックから変数に値を入れるブロックを使って、step_numberの値を1にします。
