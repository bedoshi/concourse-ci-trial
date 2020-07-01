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
1. EXTERNAL URL の変更
- ブラウザから確認できるURLに変更すること
1. 立ち上げ
```
docker-compose up -d
```
1. web でログイン
- username: admin
- password: admin
1. fly のインストール
- ブラウザでアクセスした際にDLリンクを確認して、wget等で確認するとベネ

