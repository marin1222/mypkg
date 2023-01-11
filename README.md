# mypkg
![test](https://github.com/marin1222/mypkg/actions/workflows/test.yml/badge.svg)

## 概要
ロボットシステム学の練習リポジトリ



## ブランチ
* main
  * ロボットシステム学lesson11までの内容

* lesson9
  * ロボットシステム学lesson9までの内容

* lesson10
  * ロボットシステム学lesson10まで内容

## ダウンロード
```bash
$ mkdir -p ros2_ws/src
$ cd ~/ros2_ws/src/
$ git clone https://github.com/marin1222/mypkg.git
$ cd ~/ros2_ws
$ sudo rosdep install -i --from-path src --rosdistro humble -y
$ colcon build
$ source ~/ros2_ws/install/setup.bash
```
## 入出力例
* 端末1でtalkerを起動する。
```bash
$ ros2 run mypkg talker
```
* 端末2でlistenerを起動するとtalkerで発行した情報が表示される。
```bash
$ ros2 run mypkg listener
[INFO] [1673418306.209485300] [listener]: Listen: 0
[INFO] [1673418306.696993300] [listener]: Listen: 1
・・・
```

## ノードとトピック
![image](https://raw.githubusercontent.com/marin1222/mypkg/main/rosgraph.png)
* talker・・・数字を0から0.5秒おきに1ずつ上げてcountup発行する。
* listener・・・talkerで発行された情報を表示する。

## 必要なソフトウェア
* ros2 humble

## テスト環境
* Ubuntu 22.04.1 LTS
* ros2 humble

## ライセンス
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます。
* このパッケージのコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作としたものです．
  * [ryuichiueda/my_slides robosys_2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)
* © 2022 Marin Yasuda
