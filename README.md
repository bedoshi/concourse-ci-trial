# my concourse-ci trial
とりあえずでConcourse-ciを動かしてみるまで。

## 導入
### docker/docker-compose のインストール
調べればいくらでも出てくるので勝手にやってください。
### Concourseの立ち上げ
1. wget で `docker-compose.yml` を取得する

```
wget https://raw.githubusercontent.com/starkandwayne/concourse-tutorial/master/docker-compose.yml
```

2. docker-compose.yml の編集

`CONCOURSE_EXTERNAL_URL` に `http://<IP>:8080` を設定する

3. docker-compose で立ち上げ

```
docker-compose up -d
```

4. http://<IP>:8080 にアクセスする

