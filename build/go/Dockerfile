#go version
FROM golang:1.22.0-alpine3.19
ARG backend_src_path_container

ENV BACKEND_SRC_PATH_CONTAINER $backend_src_path_container

#update & install (vimやbashを入れとくと便利）
RUN apk add --update && apk add git && apk add vim && apk add bash

# 作業ディレクトリ設定
WORKDIR ${BACKEND_SRC_PATH_CONTAINER}

# ホットリロード用にairをインストール
RUN go install github.com/cosmtrek/air@latest

# airを実行
# CMD ["air", "-c", ".air.toml"]
CMD ["sh", "-c", "echo ${BACKEND_PORT} && air -c .air.toml"]
