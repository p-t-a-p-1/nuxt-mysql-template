# イメージの指定
FROM node:14.4.0-alpine

# コンテナ内の作業ディレクトリ
WORKDIR /usr/src

# コマンド実行
# linux 最新化
# Gitインストール
# npm最新化
# vue-cliインストール
RUN apk update && \
    apk add git && \
    npm install -g npm && \
    npm install -g vue-cli