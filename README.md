# mypkg
![test](https://github.com/marin1222/mypkg/actions/workflows/test.yml/badge.svg)

## 概要
ロボットシステム学の練習リポジトリ

## ブランチ
* main
  * lesson11までの内容

* lesson9
  * lesson9までの内容

* lesson10
  * lesson10まで内容

## ダウンロード
```bash
$ mkdir -p ros2_ws/src
$ cd ~/ros2_ws/src/
$ git clone https://github.com/marin1222/mypkg.git
$ rosdep install -i --from-path src --rosdistro humble -y
$ cd ~/ros2_ws
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
* listenerが先の場合
  * listenerを先に起動すると先ずは何も表示されない
  * 別の端末でtalkerを起動するとListen: 0から表示される

## ノードとトピック
一つ一つのノード(プログラム)がトピックという流路で通信する。

## 必要なソフトウェア
* Python3
* ros2 humble

## テスト環境
* Ubuntu 22.04.1 LTS

## ライセンス
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます。
* © 2022 Marin Yasuda
