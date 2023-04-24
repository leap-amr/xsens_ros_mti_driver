# xsens_ros_mti_driver
# 概要
[xsens_mti_driver](http://wiki.ros.org/xsens_mti_driver) を ROS Noetic で使えるようにした。

# 環境
- Ubuntu 20.04
- ROS Noetic
- xsens MTi 1-series

# セットアップ
1. `~/catkin_ws/src/` にこのリポジトリをクローン
    ``` cmd
    cd ~/catkin_ws/src/
    git clone https://github.com/leap-amr/xsens_ros_mti_driver
    ```

2. ビルド
    ``` cmd
    cd ~/catkin_ws/
    catkin_make
    source ~/catkin_ws/devel/setup.bash
    ```

# 動作確認
1. 権限を与える
    xsens 本体は `/dev/ttyUSB3` にマウントされているとする

    自分の環境でどこにマウントされているかは、`ls -l /dev/serial/by-id` を実行することで調べることができる。

    ``` cmd
    sudo chmod 666 /dev/ttyUSB3
    ```

2. launch ファイルを実行してみる

    ``` cmd
    roslaunch xsens_mti_driver display.launch
    ```

# 動画
[![ROS Noetic でうごいた！やったー！](https://i9.ytimg.com/vi/AsNthXPAjJI/mqdefault.jpg?sqp=CJyfmaIG-oaymwEmCMACELQB8quKqQMa8AEB-AHUBoAC4AOKAgwIABABGGUgUyhDMA8=&rs=AOn4CLDIqS8oMxty2pk0rMCBU_zh2NHgGw)](https://youtu.be/AsNthXPAjJI)

# 参考
- [xsens_mti_driver - ROS.org](http://wiki.ros.org/xsens_mti_driver)
- [MTi 1-series Datasheet](https://www.xsens.com/hubfs/Downloads/Manuals/mti-1-series_DK3_user_manual.pdf)
- [Software & documentation - Movella](https://www.movella.com/support/software-documentation)
- [How do install uudecode?](https://askubuntu.com/questions/232440/how-do-i-install-uudecode)
- [Ros noetic support - xsens](https://base.xsens.com/s/question/0D509000016hfSICAY/ros-noetic-support?language=en_US)

# ライセンス



