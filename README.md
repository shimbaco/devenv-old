# devenv

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
