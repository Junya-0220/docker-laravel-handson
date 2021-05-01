# docker-laravel-handson

## GitHubからリポジトリをクローン

```bash

git clone git@github.com:Junya-0220/docker-laravel-handson.git

cd docker-laravel-handson

docker compose up -d --build

```

ここで、下記URLにアクセスする。

[localhost](http://127.0.0.1:10080/)

/work/public/../vendor/autoload.php を開くのに失敗してエラーになっていることを確認します。
git cloneが終わった状態では app コンテナ内に /work/vendor ディレクトリが存在しないためです。

## Laravelインストール

```bash
#mac
docker compose exec app bash
```

```bash
#app
docker compose exec app bash

cp .env.example .env

php artisan key:generate

exit
```

```bash
#mac
docker compose down
```
