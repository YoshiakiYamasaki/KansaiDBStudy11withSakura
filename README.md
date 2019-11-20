# KansaiDBStudy11withSakura
「第11回　関西DB勉強会 withさくらクラブ」用のリポジトリ：https://kansaidbstudy.connpass.com/event/144933/

## ハンズオン環境について
参加者の環境を揃えるため、さくらのクラウドを使用します。
以下の手順に従い、CentOS7のサーバーを用意し、MySQLの公式yumリポジトリのファイルをダウンロードしておいて下さい。

さくらのクラウドが使用できない方は、何らかの手段で同様の環境を準備頂ければと思います。

## サーバー環境構築(事前準備)
10分くらいで完了します。

1. さくらのクラウドで最低環境のサーバーを用意して下さい。 
    - OS: CentOS7
    - サーバープラン: 1仮想コア / 1GB
    - ディスクプラン: 20GB / SSDプラン
    - 接続先のネットワーク： インターネット
    - 作成数: 1
2. サーバーが作成できたら、接続して下さい。
Windowsユーザーの場合は[Tera Term](https://ja.osdn.net/projects/ttssh2/)など、MACユーザーの場合は標準のターミナルなどでSSH接続してください。
3. "wget"をインストールし、MySQLの公式yumリポジトリのファイルをwgetで取得して下さい。
```terminal
[ユーザー名@ホスト名 ~]$ yum install wget
[ユーザー名@ホスト名 ~]$ wget https://dev.mysql.com/get/mysql80-community-release-el7-3.noarch.rpm
[ユーザー名@ホスト名 ~]$ 
```

※MySQLの公式リポジトリは以下URLからダウンロード出来ますので、wgetを使わずに取得頂いても問題ありません。
https://dev.mysql.com/downloads/repo/yum/

※上記コマンドはCentOS7を想定したコマンドです。CentOS8を使用される場合などは、上記URLからダウンロード先を確認してコマンドを修正頂くか、上記URLから取得頂いたファイルをサーバーに配置下さい。

## 備考
当日のハンズオン実施時には、インターネット接続が必要となります。(会場でWi-Fi使用可)
