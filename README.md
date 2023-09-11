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

### VSCode 設定

[https://gist.github.com/nonz250/4a92b6c75318411080c24c8c740f9bef](https://gist.github.com/nonz250/4a92b6c75318411080c24c8c740f9bef)

VSCodeの設定が面倒な方は私の設定を公開しておきますのでこれをダウンロードして使ってみてください。

詳しくはこちらの記事を読むといいかもしれません。VSCodeの設定が自分でできる方はその環境を利用しても大丈夫です。

[https://labo.nozomi.bike/article/83](https://labo.nozomi.bike/article/83)

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
