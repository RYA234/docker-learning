```bash
# apacheコンテナを作成起動する
@RYA234 ➜ /workspaces/docker-learning (Chapter_6) $ docker run --name apa000ex19 -d -p 8089:80 httpd
2abc4b82dfb28c732733818171e6959806c19c61f90f7ca97b52a56b9e813126

# ディレクトリを移動
@RYA234 ➜ /workspaces/docker-learning (Chapter_6) $ cd Chapter6

# ホスト側のindex.htmlをapacheのhtdocsにコピーする
@RYA234 ➜ /workspaces/docker-learning/Chapter6 (Chapter_6) $ docker cp index.html apa000ex19:/usr/local/apache2/htdocs/
Successfully copied 2.05kB to apa000ex19:/usr/local/apache2/htdocs/

# apacheのhtdocs/index.htmlをホストのtoCopy/にコピーする
@RYA234 ➜ /workspaces/docker-learning/Chapter6 (Chapter_6) $ docker cp apa000ex19:/usr/local/apache2/htdocs/index.html toCopy/
Successfully copied 2.05kB to /workspaces/docker-learning/Chapter6/toCopy/

```