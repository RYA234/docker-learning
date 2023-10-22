
```bash

# コンテナを作成する
@RYA234 ➜  $ docker run --name apa000ex1 -d httpd
Unable to find image 'httpd:latest' locally
latest: Pulling from library/httpd
a378f10b3218: Pull complete 
c20157372e94: Pull complete 
073cbcfef663: Pull complete 
5f75f8a17f40: Pull complete 
39fc6f0c5be2: Pull complete 
Digest: sha256:ed6db4a8c394d075c9c59a3dbd61a3818cd302d9948057f1e19046e5bffec027
Status: Downloaded newer image for httpd:latest
9877f60831c4e60647ef96902a0de78d95286d46ebacc497d08e3d9e7f324aee

# 作成したdockerファイルを確認する
@RYA234 ➜  $ docker ps -a
CONTAINER ID   IMAGE     COMMAND              CREATED         STATUS         PORTS     NAMES
9877f60831c4   httpd     "httpd-foreground"   2 minutes ago   Up 2 minutes   80/tcp    apa000ex1

# コンテナを起動する
@RYA234 ➜  $  docker run --name apa000ex1 -d httpd
docker: Error response from daemon: Conflict. The container name "/apa000ex1" is already in use by container "9877f60831c4e60647ef96902a0de78d95286d46ebacc497d08e3d9e7f324aee". You have to remove (or rename) that container to be able to reuse that name.
See 'docker run --help'.
@RYA234 ➜  $ docker rm pa000ex1
Error response from daemon: No such container: pa000ex1
@RYA234 ➜  $ docker rm apa000ex1
Error response from daemon: You cannot remove a running container 9877f60831c4e60647ef96902a0de78d95286d46ebacc497d08e3d9e7f324aee. Stop the container before attempting removal or force remove

# コンテナを止める
@RYA234 ➜  $ docker stop apa000ex1
apa000ex1

#  コンテナを削除する
@RYA234 ➜  $ docker rm apa000ex1
apa000ex1

# 削除されたことを確認する
@RYA234 ➜$ docker ps
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES

```