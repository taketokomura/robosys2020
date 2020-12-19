
# robosys2020
ロボットシステム学課題1

## 内容
```
https://github.com/ryuichiueda/robosys_device_drivers/blob/master/myled.c を改変しデバイスドライバを作成しました。
```
## 動作環境
OS:Ubuntu 18.04

## インストール方法
```
 $ git clone https://github.com/taketokomura/robosys2020.git
```
## 実装機能
```
echo 0 > /dev/myled0　全部消灯 
echo 1 > /dev/myled0　全部を1秒間隔に点滅
echo 2 > /dev/myled0　片方を点灯
echo 3 > /dev/myled0　echo 2 > /dev/myledoを消灯し反対側を点灯
echo 4 > /dev/myled0　全部点灯
```
 ## 用意する物
・Raspberry Pi4
・ブレッドボード
・抵抗　100Ω×2
・ジャンパー線　オスーオス×2
・ジャンパー線　オスーメス×3
・LED×2
 
 ## 動作法
 ```
 make 
 ↓
 sudo insmod myled.ko
 ↓
 sudo chmod 666 /dev/myled0 
 ↓
 echo 1 > /dev/myled0 etc...
 ```
 
 ## youtube説明
 0:00 ~ 0:14 echo 1 > /dev/myled0
 0:26 ~ 0:37 echo 2 > /dev/myled0
 0:38 ~ 0:44 echo 3 > /dev/myled0
 0:45 ~ 0:55 echo 4 > /dev/myled0
 0:56 ~ 0:57 echo 0 > /dev/myled0
 
 ## 協力者
 加藤舞子
 西廣巧
 嶋田雅
 
 ## 工夫したところ
 点灯、消灯、点滅を全部できるようにし、どの動作からも変化が分かるようにした。
 
 ## youtube URL
 https://youtu.be/sFWkVtv9MPo
 
 ## ライセンス
 GNU General Public License v3.0
