# devenv

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

* [x] MySQLの設定を開発環境向けに直す
* [x] PostgreSQL入れる
* [x] Vagrantの `synced_folder` 周りの設定
* [x] PostgreSQLのタイムゾーンをJapanからUTCに変える
* [x] Foreman入れる
* [x] phantomjs入れる
* [x] zshにする
* [ ] dotfilesを持ってくる
* [ ] heroku toolbelt入れる
  * https://toolbelt.heroku.com/debian
* [ ] heroku-config入れる
  * https://github.com/ddollar/heroku-config
* [ ] https://github.com/fgrehm/vagrant-cachier 試す
* [ ] Rsync Synced Folderを試す
  * http://www.1x1.jp/blog/2014/03/vagrant-rsync-synced-folder.html
* [ ] `cap production deploy` できる感じにする
* [ ] `sshm` できる感じにする
