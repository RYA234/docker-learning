# 概要
dokcer commitでイメージを作成する

```bash
# apacheコンテナを作成する
@RYA234 ➜   $ docker run --name apa000ex22 -d -p 8092:80 httpd
3cecb74f932fa07267d72ec5b78f6cdf7ffd0c28c654939158f03584d75bbb3d

# dockerコンテナをイメージに書き出す
@RYA234 ➜   $ docker commit apa000ex22 ex22_original1
sha256:64a29fef3f2681e518db5f3439510758de551ee8b0eb35b2463cebc6c38d5e1e

# イメージを確認する
@RYA234 ➜   $ docker image ls
REPOSITORY       TAG       IMAGE ID       CREATED         SIZE
ex22_original1   latest    64a29fef3f26   4 minutes ago   168MB

```