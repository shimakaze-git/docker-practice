## MariaDB用のDockerfileについて

### Dockerイメージ作成コマンド
```
my-mariadbというコンテナイメージ名を指定

docker build -t my-mariadb .
```

### mariadbのコンテナを動作させる
```
3306番ポートで待ち受ける

docker run -it --rm -p 3306:3306 my-mariadb
```

### 参考URL
- [Dockerfileの”ENV”と”ARG”と”環境変数”について](https://techblog.recochoku.jp/1979)
- [Dockerであそぶ（６）Apache-PHP-Mariadb連携](http://tech.pjin.jp/blog/2016/01/04/docker%E3%81%A7%E3%81%82%E3%81%9D%E3%81%B6%EF%BC%88%EF%BC%96%EF%BC%89apache-php-mysql%E9%80%A3%E6%90%BA/)
