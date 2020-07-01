# my concourse-ci trial
とりあえずでConcourse-ciを動かしてみるまで。

## 導入
### docker/docker-compose のインストール
調べればいくらでも出てくるので勝手にやってください。
### Concourseの立ち上げ
1. keyの生成
```
ssh-keygen -t rsa -f ./keys/web/tsa_host_key -N ''
ssh-keygen -t rsa -f ./keys/web/session_signing_key -N ''
ssh-keygen -t rsa -f ./keys/worker/worker_key -N ''

cp ./keys/worker/worker_key.pub ./keys/web/authorized_worker_keys
cp ./keys/web/tsa_host_key.pub ./keys/worker
```

2. 立ち上げ
```
docker-compose up -d
```
