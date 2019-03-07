## Debianインストール

Debianインストール・設定メモ

### 1. インストール

[ここ](https://cdimage.debian.or.jp/)で"netinstイメージ"のISOをダウンロードしてDVDに焼く。

インストーラの指示に従ってネットに接続しインストールする。

インストールするソフトウェアの選択は使用するデスクトップ環境のみにした。

### 2. インストール後設定

```
$ su
# gpasswd sudo -a kaito
# echo 'blacklist pcspkr' >> /etc/modprobe.d/pcspkr-blacklist.conf
# LANG=C grub-mkconfig -o /boot/grub/grub.cfg
# reboot
```

再起動がかかる

```
$ sudo apt update
$ sudo apt upgrade
$ sudo apt install vim
$ sudo update-alternatives --config editor
```
