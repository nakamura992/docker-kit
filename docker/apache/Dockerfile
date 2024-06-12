# ベースイメージとしてUbuntuを使用
FROM ubuntu:latest

# パッケージの更新とインストール
RUN apt-get update && apt-get install -y \
    apache2 \
    nano

# サーバーの設定
COPY 000-default.conf /etc/apache2/sites-available/000-default.conf

# Apacheのモジュールを有効化
RUN a2enmod rewrite proxy proxy_fcgi setenvif

# 作業ディレクトリを設定
WORKDIR /var/www/html

# サーバーの起動
CMD ["apachectl", "-D", "FOREGROUND"]