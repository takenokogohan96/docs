---
{"dg-publish":true,"dg-permalink":"debian-apt","permalink":"/debian-apt/","created":"2026-01-18T12:06:39.909+09:00","updated":"2026-01-18T12:19:36.328+09:00"}
---

# パッケージリストを更新する
```
sudo apt update
```
# 全てのパッケージを更新する
```
sudo apt upgrade
```
途中聞かれる y/n でyを自動的に選択する
```
sudo apt upgrade -y
```
# パッケージをインストールする
```
sudo apt install {パッケージ名}
sudo apt install {パッケージ名} -y
```
# パッケージをアンインストールする
```
sudo apt remove {パッケージ名}
sudo apt remove {パッケージ名} -y
