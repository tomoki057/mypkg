# mypkg

[![test](https://github.com/tomoki057/mypkg/actions/workflows/test.yml/badge.svg)](https://github.com/tomoki057/mypkg/actions/workflows/test.yml)

* このリポジトリは2023年度ロボットシステム学の講義内で作成した talker と listener の2つのノードで基本的な通信を行うROS 2のパッケージをGitHubに公開したものです.

## トピック
* /countup は16ビット符号付き整数のメッセージの型を持つデータが流れるものです.

## talker.py
* talker.pyはパブリッシャを持つノードであり, 数字をカウントしてトピック /countup を通じてサブスクライバーを持つノードのlistener.pyに送信します.

## listener.py
* listener.pyはサブスクライバーを持つノードであり, トピックである /countup からメッセージを受け取り表示をします.

## talk_listen.launch.py
* talk_listen.launch.pyは talker,py と listener.py の2つのノードを一度に立ち上げるものです.

## 2つの端末で実行する場合

* 端末1
```
###実行方法###
$ ros2 run mypkg talker

###実行結果###
(なにも表示されない)
```
* 端末2
```
###実行方法###
$ ros2 run mypkg listener

###実行結果###
[INFO] [1703827280.872042590] [listener]: Listen: 0
[INFO] [1703827281.349368825] [listener]: Listen: 1
[INFO] [1703827281.849390206] [listener]: Listen: 2
[INFO] [1703827282.349319446] [listener]: Listen: 3
[INFO] [1703827282.848882394] [listener]: Listen: 4
[INFO] [1703827283.349066963] [listener]: Listen: 5
[INFO] [1703827283.848843853] [listener]: Listen: 6
[INFO] [1703827284.349116483] [listener]: Listen: 7
[INFO] [1703827284.848926822] [listener]: Listen: 8
[INFO] [1703827285.348062292] [listener]: Listen: 9
[INFO] [1703827285.849149995] [listener]: Listen: 10

...
```
## 1つの端末で実行する場合

```
###実行方法###
$ ros2 launch mypkg talk_listen.launch.py

###実行結果###
[INFO] [launch]: All log files can be found below /home/tomo0724/.ros/log/2023-12-29-00-23-03-844941-satomo724pc-680
[INFO] [launch]: Default logging verbosity is set to INFO
[INFO] [talker-1]: process started with pid [682]
[INFO] [listener-2]: process started with pid [684]
[listener-2] [INFO] [1703776984.866624614] [listener]: Listen: 0
[listener-2] [INFO] [1703776985.296741953] [listener]: Listen: 1
[listener-2] [INFO] [1703776985.796990743] [listener]: Listen: 2
[listener-2] [INFO] [1703776986.296633211] [listener]: Listen: 3
[listener-2] [INFO] [1703776986.796945494] [listener]: Listen: 4
[listener-2] [INFO] [1703776987.297226133] [listener]: Listen: 5
[listener-2] [INFO] [1703776987.796805299] [listener]: Listen: 6
[listener-2] [INFO] [1703776988.297048392] [listener]: Listen: 7
[listener-2] [INFO] [1703776988.797022717] [listener]: Listen: 8
[listener-2] [INFO] [1703776989.297141960] [listener]: Listen: 9
[listener-2] [INFO] [1703776989.796799824] [listener]: Listen: 10

...
```

## 必要なソフトウェア
* ROS2
* Python

## テスト環境
* Ubuntu 20.04.6 LTS

## 著作権・ライセンス 
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．

* このパッケージのコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作としたものです．
    * [ryuichiueda/my_slides/robosys_2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)

* © 2023 Tomoki sato
