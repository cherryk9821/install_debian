## Debianインストール

Debianインストール・設定メモ

### 1. インストール

[ここ](https://cdimage.debian.or.jp/)で"netinstイメージ"のISOをダウンロードしてDVDに焼く。

インストーラの指示に従ってネットに接続しインストールする。

インストールするソフトウェアの選択は使用するデスクトップ環境のみにした。

### 2. インストール後設定

```
$ LANG=C xdg-user-dirs-gtk-update
$ su
# gpasswd sudo -a kaito
# echo 'blacklist pcspkr' >> /etc/modprobe.d/pcspkr-blacklist.conf
# LANG=C grub-mkconfig -o /boot/grub/grub.cfg
# reboot
```

再起動がかかる

最初のコマンドでディレクトリ名を英語に変えたとき、"blueman-service"のダウンロードフォルダのエラーが起こったら以下のコマンドを実行する。

```
gsettings set org.blueman.transfer shared-path '/home/user_name/Downloads'
```

上のコマンドの"user_name"の部分は自分のユーザー名に置き換える。

```
$ sudo apt update
$ sudo apt upgrade
$ sudo apt install vim git
$ sudo update-alternatives --config editor
```

### 3. Go言語インストール

[ここ](https://golang.org/dl/)でバイナリをダウンロードする。

Linux用バイナリをダウンロード後以下のコマンドを実行する。

```
$ sudo tar -C /usr/local -xzf go1.12.linux-amd64.tar.gz
```

### 4. VS Codeインストール

[ここ](https://code.visualstudio.com/docs/setup/linux)を参照して64bitのdebパッケージをダウンロードし以下のコマンドを実行する。

```
$ sudo apt install ./<file>.deb
```

VS Codeの設定は[ここ](https://github.com/cherryk9821/install_vscode)を参照。
