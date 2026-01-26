---
{"dg-publish":true,"dg-permalink":"ubuntu-apt","permalink":"/ubuntu-apt/","created":"2026-01-26T14:14:54.317+09:00","updated":"2026-01-26T14:23:35.331+09:00"}
---

## パッケージリストを更新する
```
sudo apt update
```
## 全てのパッケージを更新する
```
sudo apt upgrade
```
y/nをyで自動的に進める
```
sudo apt upgrade -y
```
## パッケージをインストールする
```
sudo apt install {パッケージ名}
```
## インストール済みのパッケージ名を表示する
すべてのパッケージを表示する
```
apt list --installed
```
特定のパッケージ名（なければ表示なし。あれば installed）
```
apt list --installed ｛パッケージ名｝
```
## パッケージをアンインストールする
```
sudo apt remove {パッケージ名}
```
