# non-labo-ch

のんラボ用の環境プロジェクトです。

youtubeチャンネルはこちら [https://www.youtube.com/channel/UCzpY7GBbWJFHA3JVjkgbAjA](https://www.youtube.com/channel/UCzpY7GBbWJFHA3JVjkgbAjA)

## 環境

|-|-|
|---|---|
|Nginx|1.19系|
|PHP|8.2系|
|MySQL|8.0系|
|Composer|2.5系|
|Node|latest|

## コマンド

### 初めてこのリポジトリを使う場合

```shell script
cp docker-compose.yml.example docker-compose.yml

docker-compose build
```

### 起動

```bash
docker-compose up -d
```

### 停止

```bash
docker-compose down
```
