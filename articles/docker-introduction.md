---
title: "Dockerを学ぶ"
emoji: "🐳"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["Docker", "Dockerfile", "DockerImage", "DockerContainer"]
published: true
---

Docker を学び始めたので、学んだことをまとめていきます。
間違って理解していることなどありましたらご指摘いただけると大変ありがたいです。

# Docker とは

> Docker はアプリケーションを開発（developing）、移動（shipping）、実行（running）するためのオープンなプラットフォームです。
> Docker はインフラストラクチャとアプリケーションを切り離すため、ソフトウェアを短時間で提供できます。Docker があれば、アプリケーションを管理するのと同じ方法で、あなたのインフラも管理できます。Docker 的な手法を最大限活用しますと、テストやコードのデプロイを素早くできますので、コードを書いてから、プロダクション（実行環境）で動かすまでにかかる時間を著しく軽減できます。

[What is Docker? | Docker Documentation](https://docs.docker.jp/get-started/overview.html)

# Docker の基本用語

### Docker Image

Docker Image は、Docker コンテナを作成するためのテンプレートのようなもの。
Docker Image は、Docker Hub というサービスで公開されているものが多く、Docker Hub から Image をダウンロードして、その Image を元にコンテナを作成することができる。

### Docker File

Dockerfile は、Docker Image を作成するための設計図のようなもの。
Docker Image を作成するためのコマンドが記述されている。

### Docker Container

Docker Container は、Docker Image を元に作成されたコンテナのこと。
作成されたコンテナを起動することで、そのコンテナ内でアプリケーションを実行することができる。

# Docker の基本コマンド:

### "docker run" コマンド

Docker の "docker run <Image 名>" コマンドを実行すると、Docker Hub から指定した Image をダウンロードし、その Image を元にコンテナを作成し、そのコンテナを起動することができる。

### "docker exec -it" コマンド

Docker の "docker exec -it <コンテナ ID or コンテナ名> bash" コマンドを実行すると、既存のコンテナ内で bash シェルを起動し、そのシェルを操作することができる。
もしくは"docker run -it <コンテナ名> bash"コマンドを実行することで、新規にコンテナを作成し、そのコンテナ内で bash シェルを起動することも可能。

### "docker ps" コマンド

Docker の "docker ps" コマンドを実行すると、現在起動しているコンテナの一覧を表示することができる。

### "docker images" コマンド

Docker の "docker images" コマンドを実行すると、現在ローカルに保存されている Docker Image の一覧を表示することができる。

### "docker stop" コマンド

Docker の "docker stop <コンテナ ID or コンテナ名>" コマンドを実行すると、指定したコンテナを停止することができる。

### "docker rm" コマンド

Docker の "docker rm <コンテナ ID or コンテナ名>" コマンドを実行すると、指定したコンテナを削除することができる。

### "docker rmi" コマンド

Docker の "docker rmi <Image 名>" コマンドを実行すると、指定した Image を削除することができる。

### "docker exit" コマンド

Docker の "docker exit" コマンドを実行すると、コンテナ内の bash シェルを終了することができる。

### "docker detach" コマンド

Docker の "docker detach" コマンドを実行すると、コンテナ内の bash シェルを終了せずに、コンテナから抜けることができる。
exit コマンドとの違いは、exit コマンドを実行するとコンテナ自体が停止するが、detach コマンドを実行するとコンテナは停止せずに起動し続ける。
基本的には exit コマンドを実行することが多いらしい。

:::message
今後も追記していく予定です。
:::
