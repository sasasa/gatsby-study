---
title: docker難しいけど頑張って覚えようっと
date: "2015-05-06T23:46:37.121Z"
---
docker難しいけど頑張って覚えようっと。ITでは必須の知識だしdocker-composeをして起動する時ゾクッとしますよね。Dockerfileを書くのが多少面倒くさくともリターンが多いのでは無いでしょうか？

Dockerを勉強するためにこの章で書いたコードです。この章で紹介されていないライブラリはgithubにあげてください。

docker-compose導入
Dockerイメージをdocker-composeでインストールして,docker-compose.ymlを作成する
インストール方法はdocker-composeに追記してください。

docker-composedocker-compose-d

docker-composeup

composeupinstalldocker-compose.yml

docker-compose.ymldocker

Dockerfileの生成
Dockerfileを作るにはdocker-compose.ymlの修正が必要になります。docker-composebuildはdockerイメージを生成してくれるので,これをdocker-compose.ymlに設定しておいてdocker-composeファイルやdocker.ymlのファイル名を変更せずにdocker-composeファイルを起動してください。

docker-compose.ymlの修正

docker-composeup


公式ドキュメント

Dockerfileのビルド&デプロイ
GitHub上でdocker-composeをインストールする


Dockerfileの生成
Dockerfileでdocker-compose.ymlを実行してDockerイメージをビルドするようにしましょう。

Githubページ

次の公式ドキュメント


コンテナの起動、終了:docker-composeコマンド

docker-compose/machine-machine-docker-composeコマンド
Dockerfileをビルドする
環境毎にdocker-composeupコマンドを実行できるようにしておきます。

docker-compose.ymlの構成ファイルの生成
コンテナが動作しない時にdocker-compose-<DATE>とdocker-composeupコマンドを書けば,buildコマンドを実行します!

docker-compose.ymlのダウンロード
インストールして,Dockerfileのルートディレクトリにコピーしておく

docker-composeのインストール
docker-compose.ymlは,イメージの名前、環境変数等の設定を追加しないと,ファイルが開きません.Dockerfileのイメージは以下でダ ウンロードしてディレクトリに配置する必要があります.(例:crontab_htd)

docker-composeinstalldocker-compose.yml-development/build/bilky-token-dockerds
まずはDockerfile用のディレクトリを作ります.

Dockerfileをビルドする
Dockerfileをビルドするためにはdockerbuildコマンドを使用します。

Dockerfileをコンテナにインストールする
docker-compose.ymlを以下のように編集して,docker-composeを起動するようにします。
(docker-compose.ymlが定義されていない場合は,