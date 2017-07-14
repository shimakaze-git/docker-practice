## Docker練習用リポジトリ

### 環境構築方法

以下のURLを参考にする
- [DockerをLinux(Ubuntu 14.04 LTS)にインストールする方法と解説](http://tracpath.com/works/devops/how_to_install_the_docker/)

### Docker動作


Dockerホスト側とコンテナ側でディレクトリを共有させる
```
Apacheの最新版を動かす


docker run -it --rm -p 80:80 -v /home/admin/httpd/public-html:/usr/local/apache2/htdocs/ httpd:latest
```

終了したコンテナの設定ファイル等をコピーする
```
$ docker ps -a
CONTAINER ID        IMAGE               COMMAND              CREATED              STATUS                          PORTS               NAMES
bab2b9bd0fbf        httpd:latest        "httpd-foreground"   About a minute ago   Exited (0) About a minute ago                       reverent_ptolemy


コンテナID[bab2b9bd0fbf]のコンテナ内部からファイルをコピー


ローカルディレクトリ上にhttpd.confを保存


$ docker cp bab2b9bd0fbf:/usr/local/apache2/conf/httpd.conf ./
```

### Dockerfile作成

コマンド一覧
- FROM : 作成するイメージのベースとなるコンテナイメージを指定
- COPY : ホストのファイルをコンテナイメージ内部にコピー

```
カレントディレクトリ上にある「Dockerfile」を使用してビルドを開始。-t オプションはコンテナイメージにつける名前


docker build -t my-httpd .
```
