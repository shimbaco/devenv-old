# devenv-old

## もう使ってません

以前はVagrantで動かしていたUbuntuの中に開発環境を作ってましたが、
以下の出来事があったので再びMacで開発環境を作ることにしました。

* `bundle open` が使えない
* 「gulp-watch」や「nodemon」を使うとき、ファイルの変更が検知されない

新しいdevenv: https://github.com/shimbaco/devenv

---

[![Stories in Ready](https://badge.waffle.io/bojovs/devenv.svg?label=ready&title=Ready)](http://waffle.io/bojovs/devenv)

Vagrant + Ansibleで作られた開発環境です。


## インストールされるもの

* Ubuntu 14.04
* Ruby
  * rbenv
* Node.js
* MySQL
* PostgreSQL
* Redis
* ImageMagick


## 動かし方

```
$ mkdir ~/dev // ゲストOSとのディレクトリ共有に使用
$ git clone git@github.com:bojovs/devenv.git
$ cd devenv
$ vagrant up
```


## Vagrantのコマンド

* vagrant upしたあと、Ansibleのプロビジョニングのみ実行する

```
$ vagrant provision
```

* 再起動する

```
$ vagrant reload
```


## TODO

[Waffle.io](https://waffle.io/bojovs/devenv) で管理してます。
