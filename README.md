# docker-lemp1

## 起動手順
1. phpコンテナ内のuidをhost側のuidに合わせる
    1. host側でidコマンドを実行する
    1. 上記手順で調べたuid=XXXXの値を/php/Dockerfile内の`ARG DOCKER_UID`に設定する
1. Dockerを起動する
    ```
    docker-compose up -d
    ```

## メモ
- htmlディレクトリがnginx/phpコンテナのドキュメントルート`/var/www/html`にマウントされている
- phpコンテナに接続する方法
    ```
    docker-compose exec php bash
    ```
- phpMyAdminにアクセスる方法
  - ブラウザで下記アドレスにアクセスする
      - http://localhost:10040

## 参考
- [Docker ComposeでNginxとphpを連携する][link1]


[link1]:https://zukucode.com/2019/06/docker-compose-nginx-php.html
