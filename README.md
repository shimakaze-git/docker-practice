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
