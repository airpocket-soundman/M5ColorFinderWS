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
