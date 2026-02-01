---
{"dg-publish":true,"dg-permalink":"ubuntu-apt","permalink":"/ubuntu-apt/","created":"2026-01-18T06:42:52.000+09:00","updated":"2026-02-01T14:18:46.489+09:00"}
---

## パッケージリストを更新する
```
sudo apt update
```
## 全てのパッケージを更新する
```
# オプションなし
sudo apt upgrade

# y/nをyで自動的に進める
sudo apt upgrade -y
```
## パッケージをインストールする
```
sudo apt install {パッケージ名}
sudo apt install {パッケージ名} -y
```
## インストール済みのパッケージ名を表示する
```
# 全部
apt list --installed

# 特定のパッケージ名（なければ表示なし。あれば[installed]）
apt list --installed ｛パッケージ名｝
```
## パッケージをアンインストールする
```
sudo apt remove {パッケージ名}
sudo apt remove {パッケージ名} -y
```
