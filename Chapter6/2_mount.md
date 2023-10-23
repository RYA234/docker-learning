#　マウントの種類
## ボリュームマウント
仮で使いたい場合や、滅多に触らないが、消してはいけないファイル
難しい


## バインドマウント
頻繁に触りたいファイル（ディレクトリ）を指定する


# バインドマウントの方法

```bash
# -vオプションでボリュームマウントする
docker run --name apa000ex20 -d -p 8090:80 -v /workspaces/docker-learning/Chapter6/toCopy:/usr/local/
apache2/htdocs httpd

# localhost:8090を開いて　[index of]と表示される。

# toMountディレクトリにindex.htmlをコピペすると index.htmlの内容が反映される。



```