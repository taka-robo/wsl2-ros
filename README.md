# wsl2-ros
wsl2でROSを使うセットアップ

### xサーバーを使ってGUIを使えるようにする
powershellで
``` powershell
wsl --set-default-version 2
```
wslを起動
``` bash
# Xサーバー通信用のアプリ群を入れる
sudo apt update
sudo apt install x11-apps -y 
# 環境変数を設定する
## rvizがXサーバーと正しく通信できるようにする
echo 'export LIBGL_ALWAYS_INDIRECT=""' >> ~/.bashrc 
## GazeboがXサーバーと正しく通信できるようにする
echo 'export GAZEBO_IP=127.0.0.1' >> ~/.bashrc
source ~/.bashrc 
```
vcxsrvのインストール
https://sourceforge.net/projects/vcxsrv/

### ROSのインストール
[公式サイト](http://wiki.ros.org/noetic/Installation/Ubuntu)にそって
