# README

## php関連のコマンドを使用する場合は下記のコマンドでコンテナ内に入ってから実行を行う
- docker exec -it コンテナ名 bash <br>
例： `docker exec -it php-apache bash`<br>

## Laravelのインストール
- コンテナを立ち上げる前にLaravelをインストールする<br>
`docker-compose run php composer create-project --prefer-dist laravel/laravel .`<br>

## コンテナの立ち上げ
`docker-compose up -d`<br>

## DBの接続設定とdataの永続化
-DBの接続設定<br>
> docker-compose.ymlファイルにenvironment:で記載の環境変数をLaravelのenvファイルに設定<br>

-dataの永続化について
> -githubにdataフォルダーをアップロードしていないため、個人で設定してください。<br>
> docker-compose.ymlファイルにvolumeで読み込むように設定<br>
