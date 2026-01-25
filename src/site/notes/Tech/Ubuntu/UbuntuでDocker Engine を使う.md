---
{"dg-publish":true,"dg-permalink":"ubuntu-docker","permalink":"/ubuntu-docker/","created":"2026-01-25T15:14:44.419+09:00","updated":"2026-01-18T23:43:03.517+09:00"}
---

基本dockerdocs公式の [Install Docker Engine on Ubuntu](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository) の通り

# リポジトリ周りを設定する
```
# Add Docker's official GPG key:
sudo apt update
sudo apt install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
sudo tee /etc/apt/sources.list.d/docker.sources <<EOF
Types: deb
URIs: https://download.docker.com/linux/ubuntu
Suites: $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}")
Components: stable
Signed-By: /etc/apt/keyrings/docker.asc
EOF

sudo apt update
```
# Dockerをインストールする
```
sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
# Dockerが起動していることを確認する
```
sudo systemctl status docker
```
# イメージとコンテナを表示する
```
# イメージ
docker images

# コンテナ
docker ps

# コンテナ（停止中含む）
docker ps -a
```
# イメージを取得する
```
# Docker Hub からDLする
docker pull ｛リポジトリ名｝
```
# # イメージとコンテナを削除する
```
# コンテナ
docker rm {コンテナID}

# イメージ
docker rmi {イメージ名}
```
# Docker Compose で コンテナを起動する
1. あらかじめ `docker-compose.yml` を作成する
2. コマンドを入力する
```
# イメージを更新してコンテナを起動する
docker compose up --build

# バックグラウンドで起動する
docker compose up --build -d
```