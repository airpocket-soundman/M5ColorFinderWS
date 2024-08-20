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
  
### M5Burnerのダウンロードとインストール
  
M5Bunerを以下のサイトからダウンロードします。  
https://docs.m5stack.com/en/download
  
<img src="https://github.com/airpocket-soundman/M5ColorFinderWS/blob/main/image/burner_download.png?raw=true" alt="burner download"><br>  
  
ダウンロードしたファイルを解凍しツールを実行します。

# M5いろあつめ　制作

##