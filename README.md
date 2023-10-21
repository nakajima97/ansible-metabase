# 概要
Ansibleを使ってMetabaseを構築してみたのでその記録

# やったこと
- rootless dockerのインストール

# 妥協点
## Rootless Dockerのインストールに関して
以下のコマンドがansibleでの書き方が分からず妥協  
.bashrc編集後の読み込み方法が分からない
```
. ~/.bashrc
loginctl disable-linger rootless-docker
loginctl enable-linger rootless-docker
/usr/bin/dockerd-rootless-setuptool.sh install -f
systemctl --user restart docker
systemctl --user is-active docker
```