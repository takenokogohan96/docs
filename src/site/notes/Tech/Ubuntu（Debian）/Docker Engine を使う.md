---
{"dg-publish":true,"dg-permalink":"ubuntu-docker","permalink":"/ubuntu-docker/","created":"2026-01-18T13:33:05.980+09:00","updated":"2026-01-18T13:52:54.967+09:00"}
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
# 持ってるイメージを表示する
```
docker images
```
# 持ってるコンテナを表示する
```
＃　起動中のコンテナ
docker ps

# 停止中も含めすべてのコンテナ
docker ps -a
```
# コンテナを削除する
```
docker rm {コンテナID}
```
# イメージを削除する
```
docker rmi {イメージ名}
```