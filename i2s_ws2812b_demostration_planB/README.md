これは、nRF52832のeasyDMAのI2Sを使ってWS2812B LED アレイを制御するプログラムのサンプルです。

Nordic nRF5 SDK 11.0.0-2.alpha_bc3f6a0 と nRF52-DK (PCA-10040) (CPU version は Engineering B (QFAA-BA0))の組み合わせで動作を確認しています.
SDKパスの下のexamplesの下に、フォルダを作成し、その下にi2s_ws2812b_demonstration_planB等の名前で本ディレクトリ配下を展開してください。
例：C:\nRF52832\nRF5_SDK_11.0.0-2.alpha_bc3f6a0\examples\my_work\i2s_ws2812b_demonstration_planB\main.c

LEDアレイと5V電源、そして3.3V→5V変換の信号レベル変換が必要です。
WS2812Bベースの(240個からなる)LEDテープを使っています。
https://www.switch-science.com/catalog/2100/ 
Adafruit社のneopixel LEDと互換性がある筈です。
信号レベル変換にはTXB0104ベースのものを使っています。
https://www.switch-science.com/catalog/1466/
https://www.sparkfun.com/products/11771

P0.25に出力されたSDOUT信号をTXB0104の入力に、TXB0104の出力をLEDアレイのDIに接続して下さい。

--------------------------------------------------------------

 This is a sample program to drive WS2812B LED array by Nordic Semiconductor nRF52832 with easyDMA based I2S.
 
It works with Nordic nRF5 SDK 11.0.0-2.alpha_bc3f6a0 and nRF52-DK (PCA-10040) with CPU version Engineering B (QFAA-BA0).
Make a folder under "example" in SDK installed path. ANd extract i2s_ws2812b_demonstration directory in it.
Example：C:\nRF52832\nRF5_SDK_11.0.0-2.alpha_bc3f6a0\examples\my_work\i2s_ws2812b_demonstration\main.c

I also used LED array, 5V power supply and (3.3V to 5V) signal level converter.
The LED array is WS2812B based 240 LEDs array purchased from Switch-Science, Inc.
https://www.switch-science.com/catalog/2100/ 
It will compatible with Adafruit neopixel LED array.
The signal level converter is TXB0104 based.
https://www.switch-science.com/catalog/1466/
https://www.sparkfun.com/products/11771

Connect SDOUT signal line on P0.25 to signal buffer input and connect signal buffer output to control line DI of LED array. 


