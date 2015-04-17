# devenv

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
