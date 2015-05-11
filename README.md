# devenv-old

## もう使ってません

以前はVagrantで動かしていたUbuntuの中に開発環境を作ってましたが、
以下の出来事があったので再びMacで開発環境を作ることにしました。

* `bundle open` が使えない
* 「gulp-watch」や「nodemon」を使うとき、ファイルの変更が検知されない

新しいdevenv: https://github.com/shimbaco/devenv

---

[![Stories in Ready](https://badge.waffle.io/shimbaco/devenv.svg?label=ready&title=Ready)](http://waffle.io/shimbaco/devenv)

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
$ git clone git@github.com:shimbaco/devenv.git
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

[Waffle.io](https://waffle.io/shimbaco/devenv) で管理してます。
