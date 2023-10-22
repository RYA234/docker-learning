```bash
# apacheのコンテナを３つ作る
# 違いはクライアント側のポート番号を変える
#  8080:80→ クライアント側のポート番号は8080 コンテナ側のポート番号は80
@RYA234 ➜   $ docker run --name apa000ex3 -d -p 8081:80 httpd
8d7a5344920c6b5fd476138477d96a8066fc545a01b79f09093c92f1791b42f5
@RYA234 ➜   $ docker run --name apa000ex4 -d -p 8082:80 httpd
4efa0227a214f1a8eae5e944e825a99c99dacb67052b34d64736ffff98356c00
@RYA234 ➜   $ docker run --name apa000ex5 -d -p 8083:80 httpd
8d9f3313bfc7f5b4fa9de45a0105a07461379be6b6e5d95aee5d1bf55f9ff954
# コンテナの状態を確認する
@RYA234 ➜   $ docker ps
CONTAINER ID   IMAGE     COMMAND              CREATED          STATUS          PORTS                                   NAMES
8d9f3313bfc7   httpd     "httpd-foreground"   25 seconds ago   Up 24 seconds   0.0.0.0:8083->80/tcp, :::8083->80/tcp   apa000ex5
4efa0227a214   httpd     "httpd-foreground"   42 seconds ago   Up 41 seconds   0.0.0.0:8082->80/tcp, :::8082->80/tcp   apa000ex4
8d7a5344920c   httpd     "httpd-foreground"   50 seconds ago   Up 49 seconds   0.0.0.0:8081->80/tcp, :::8081->80/tcp   apa000ex3

# 3つのコンテナを閉じる
@RYA234 ➜   $ docker stop apa000ex3
apa000ex3
@RYA234 ➜   $ docker stop apa000ex4
apa000ex4
@RYA234 ➜   $ docker stop apa000ex5
apa000ex5

# 3つのコンテナを削除
@RYA234 ➜   $ docker rm apa000ex3
apa000ex3
@RYA234 ➜   $ docker rm apa000ex4
apa000ex4
@RYA234 ➜   $ docker rm apa000ex5
apa000ex5

# コンテナの状態を確認
@RYA234 ➜   $ docker ps
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES

```
