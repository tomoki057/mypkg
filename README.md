# mypkg

[![test](https://github.com/tomoki057/mypkg/actions/workflows/test.yml/badge.svg)](https://github.com/tomoki057/mypkg/actions/workflows/test.yml)

* このレポジトリは2023年度ロボットシステム学の講義内で作成したtalkerとlistenerの2つのノードで基本的な通信を行うROS 2プログラミングをGitHubに公開したものです。

#### 2つの端末で実行する場合

* 端末1
```
$ ros2 run mypkg talker
(なにも表示されない)
```
* 端末2
```
$ ros2 run mypkg listener

...
```
#### 1つの端末で実行する場合

```
$ ros2 launch mypkg talk_listen.launch.py
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
* ROS2 foxy
* Python

## テスト環境
* Ubuntu 20.04.6 LTS

## 著作権・ライセンス 
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．

* このパッケージのコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作としたものです．
    * [ryuichiueda/my_slides/robosys_2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)

* © 2023 Tomoki sato
