# イメージの指定
FROM node:14.4.0-alpine

# コンテナ内で cd /app しているようなもの
WORKDIR /usr/src/app

# コマンド実行
# linux 最新化,gitのインストール、npm最新化、vue-cli インストール　をしている。
RUN apk update && \
    apk add git && \
    npm install -g npm && \
    npm install -g vue-cli