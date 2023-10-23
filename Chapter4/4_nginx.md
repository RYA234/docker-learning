```bash
#  nginxのコンテナを作成、起動する
@RYA234 ➜  $ docker run --name nginx000ex06 -d -p 8084:80 nginx
Unable to find image 'nginx:latest' locally
latest: Pulling from library/nginx
a378f10b3218: Already exists 
4dfff0708538: Pull complete 
2135e49ace4b: Pull complete 
c843f6b280ce: Pull complete 
6f35ab6f1400: Pull complete 
6c538b49fa4a: Pull complete 
d57731fb9008: Pull complete 
Digest: sha256:b4af4f8b6470febf45dc10f564551af682a802eda1743055a7dfc8332dffa595
Status: Downloaded newer image for nginx:latest
a999bec779d145d8902470cb4c0430dc714bbe9024b8355fe32e548f45d99150

# nginxコンテナができたか確認する
@RYA234 ➜  $ docker ps
CONTAINER ID   IMAGE     COMMAND                  CREATED          STATUS          PORTS                                   NAMES
a999bec779d1   nginx     "/docker-entrypoint.…"   23 seconds ago   Up 22 seconds   0.0.0.0:8084->80/tcp, :::8084->80/tcp   nginx000ex06
# nginxコンテナを停止する
@RYA234 ➜  $ docker stop nginx000ex06
nginx000ex06
# nginxコンテナを削除する
@RYA234 ➜  $ docker rm nginx000ex06
nginx000ex06
#  コンテナが削除されたか確認する
@RYA234 ➜  $ docker ps -a
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES


```