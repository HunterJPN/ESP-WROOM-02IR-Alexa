# ESP-WROOM-02-IR-Alexa

#H1 ”SWITCHSCIENCE ESPr® IR 赤外線リモコン”と”Amazon Echo”を使ってAlexaからリモコンコントロール

※注意）マークダウンに慣れていませんので、醜いのをご了承ください。

ESP-WROOM-02 Wifiモジュール搭載なESP8266を使い、Alexaのスマートホームデバイスとしてエミュレータによりデバイス登録を実現して、スマートホームを楽しむ第一弾。
「Alexaに呼び掛けてAlexaを音声リモコン代わりにしよう」

#H2　準備するもの
”SWITCHSCIENCE ESPr® IR 赤外線リモコン”
https://www.switch-science.com/catalog/2740/

”FTDI USBシリアル変換アダプター（5V/3.3V切り替え機能付き）”
https://www.switch-science.com/catalog/1032/

下準備として以下を１度済ませておくことを推奨します。
http://trac.switch-science.com/wiki/ESP-IR

#H2 動作環境
Arduino　IDE　1.8.5
ボードマネージャ：esp8266 by ESP8266 Community をインストール
  バージョンは2.3.0で動作確認

ライブラリインストール
  "fauxmoESP" の ESPAsyncTCP by Hristo Gochkov ESP8266
  https://bitbucket.org/xoseperez/fauxmoesp
  FauxmoESPライブラリバージョンも2.3.0にする。

リモコンのパターン情報は
IRremoteESP8266-> IRrecvDumpV2 とかで・・・。

#H2　参考

”ESPr IR 赤外線リモコンでエアコンの電源を操作してみました。”
http://mag.switch-science.com/2016/08/22/espr-ir-aircon/
  赤外線の長い信号を扱うために拝借しました（sendIRData部分はそのまま使っています）。

Patrick Harrerさんのソースを（まるまる）ベースとさせていただきました。
https://bitbucket.org/xoseperez/fauxmoesp/issues/39/generation-2-devices-support
