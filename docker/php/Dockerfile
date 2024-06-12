# ベースイメージとしてPHP 8.2-FPMを使用
FROM php:8.2-fpm

# 必要なパッケージをインストールし、PHP拡張機能をインストール
RUN apt-get update && apt-get install -y \
    libpng-dev \
    libjpeg-dev \
    libfreetype6-dev \
    libonig-dev \
    libxml2-dev \
    zip \
    nano \
    && docker-php-ext-install pdo_mysql mbstring exif pcntl bcmath gd mysqli

# 作業ディレクトリを設定
WORKDIR /var/www/html

# 設定ファイルのコピー
COPY php.ini /usr/local/etc/php/
