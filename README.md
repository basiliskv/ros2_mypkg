
# ROS2マイパッケージ

これは、パブサブ（パブリッシャ-サブスクライバ）パターンを使用して、2つのノード間で基本的な通信を行うROS 2のパッケージです。
# テスト
![test](https://github.com/basiliskv/ros2_mypkg/actions/workflows/test.yml/badge.svg)

## インストール

1. システムにROS 2がインストールされていることを確認してください。未インストールの場合は、[ROS 2のインストール手順](https://docs.ros.org/en/foxy/Installation.html)に従ってください。

2. このリポジトリをROS 2のワークスペースにクローンします。

   ```bash
   $ git clone https://github.com/basiliskv/ros2_mypkg.git
   ```

3. ROS2のトップディレクトリでパッケージをビルドします。

   ```bash
    $ colcon build
   ```

4. ROS 2のワークスペースをソースに指定します。

   ```bash
   $ source ~/.bashrc
   ```

## 使用方法

### 単独での実行

1. ターミナルを開き、talkerノードを実行します。

   ```bash
   $ ros2 run mypkg talker.py
   ```

2. 別のターミナルを開き、listenerノードを実行します。

   ```bash
   $ ros2 run mypkg listener.py
   ```

   リスナーは、トーカーから受け取ったカウントを表示します。
   ```bash
    [INFO] [listener]: Listen: 0
    [INFO] [listener]: Listen: 1
    [INFO] [listener]: Listen: 2
   ```

### Launchファイルを使用して同時に実行

1. 下記のコマンドを実行して、`talk_listen.launch.py`を使用してトピックのパブリッシャとサブスクライバを同時に起動します。

   ```bash
   $ ros2 launch mypkg talk_listen.launch.py
   ```

   これにより、トピックのパブリッシャ（talker）とサブスクライバ（listener）が同時に起動します。

## ソフトウェア要件

このパッケージを使用するには、以下のソフトウェアが必要です。

- Python
- ROS 2

## テスト環境

このパッケージは以下の環境でテストされています。

- Ubuntu 22.04.3 LTS

## ライセンス
  * このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．
  * このパッケージのコードの一部は，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作としたものです．
      * [https://ryuichiueda.github.io/my_slides/robosys_2022/lesson7.html#/](https://ryuichiueda.github.io/my_slides/robosys_2022/lesson4.html#/)
      * [https://ryuichiueda.github.io/my_slides/robosys_2022/lesson8.html#/](https://ryuichiueda.github.io/my_slides/robosys_2022/lesson5.html#/)
      * [https://ryuichiueda.github.io/my_slides/robosys_2022/lesson9.html#/](https://ryuichiueda.github.io/my_slides/robosys_2022/lesson6.html#/)
      * [https://ryuichiueda.github.io/my_slides/robosys_2022/lesson10.html#/](https://ryuichiueda.github.io/my_slides/robosys_2022/lesson6.html#/)
      * [https://ryuichiueda.github.io/my_slides/robosys_2022/lesson11.html#/](https://ryuichiueda.github.io/my_slides/robosys_2022/lesson6.html#/)

