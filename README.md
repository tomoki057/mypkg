# mypkg
こちらは千葉工業大学未来ロボティクス学科のロボットシステム学２０２３の授業で製作したものです

* ROS2のインストールがまだの方は先にインストールをお願いします
* ROS2のインストールがお済の方は以下のコードでクローンを行ってください
```
$ git clone https://github.com/515629/mypkg.git
```

## talker.py
* 数字をカウントして、トピック/countupを通じてメッセージを送信するパブリッシャを持つノードです
    * メッセージの型は16ビット符号つき整数です

## listener.py
* /countupからメッセージをもらって表示するサブスクライバを持つノードです

## talk_listen.launch.py
* talker.pyとlistener.pyを一度に立ち上げることができます

## 使用方法と結果

#### 端末を2つ使って実行する

* 端末1
```
$ ros2 run mypkg talker
(なにも表示されないです)
```
* 端末2
```
$ ros2 run mypkg listener
[INFO] [1703247924.927275467] [listener]: Listen: 26
[INFO] [1703247925.405913627] [listener]: Listen: 27
[INFO] [1703247925.905327838] [listener]: Listen: 28
[INFO] [1703247926.406000302] [listener]: Listen: 29
[INFO] [1703247926.905997234] [listener]: Listen: 30
[INFO] [1703247927.405712175] [listener]: Listen: 31
[INFO] [1703247927.905686033] [listener]: Listen: 32
[INFO] [1703247928.405870943] [listener]: Listen: 33
[INFO] [1703247928.906206418] [listener]: Listen: 34
[INFO] [1703247929.405930550] [listener]: Listen: 35
[INFO] [1703247929.905829181] [listener]: Listen: 36
[INFO] [1703247930.405274588] [listener]: Listen: 37
[INFO] [1703247930.906189735] [listener]: Listen: 38
(Ctrl+Cを行うまで出力し続けます)
```
#### 端末を1つ使って実行する

```
$ ros2 launch mypkg talk_listen.launch.py
[INFO] [launch]: All log files can be found below /home/tokojun/.ros/log/2023-12-22-21-36-45-552193-jusomaru-527
[INFO] [launch]: Default logging verbosity is set to INFO
[INFO] [talker-1]: process started with pid [528]
[INFO] [listener-2]: process started with pid [530]
[listener-2] [INFO] [1703248606.297414304] [listener]: Listen: 0
[listener-2] [INFO] [1703248606.786162760] [listener]: Listen: 1
[listener-2] [INFO] [1703248607.285348985] [listener]: Listen: 2
[listener-2] [INFO] [1703248607.785775273] [listener]: Listen: 3
[listener-2] [INFO] [1703248608.286045472] [listener]: Listen: 4
[listener-2] [INFO] [1703248608.784793378] [listener]: Listen: 5
[listener-2] [INFO] [1703248609.285026779] [listener]: Listen: 6
[listener-2] [INFO] [1703248609.785483579] [listener]: Listen: 7
[listener-2] [INFO] [1703248610.286174203] [listener]: Listen: 8
[listener-2] [INFO] [1703248610.785933533] [listener]: Listen: 9
[listener-2] [INFO] [1703248611.285891717] [listener]: Listen: 10
(Ctrl+Cを行うまで出力し続けます)
```

## 必要なソフトウェア
* ROS2 foxy

## テスト環境
* Ubuntu 20.04.6 LTS

## 著作権・ライセンス 
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．

* このパッケージのコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作としたものです．
    * [ryuichiueda/my_slides/robosys_2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)

* © 2023 Tomoki sato
