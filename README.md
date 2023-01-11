# mypkg
![test](https://github.com/marin1222/mypkg/actions/workflows/test.yml/badge.svg)

## 概要
ロボットシステム学の練習リポジトリ

## ブランチ
* main
  * lesson11まで

* lesson9
  * lesson9まで

* lesson10
  * lesson10まで

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
$ 

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
