---
{"dg-publish":true,"dg-permalink":"rtx1210-consoleport","permalink":"/rtx1210-consoleport/","created":"2026-01-18T00:10:11.433+09:00","updated":"2026-01-18T00:52:05.519+09:00"}
---


# 用意するもの
- Tera Term（[Github](https://github.com/TeraTermProject/teraterm/releases)）
- RJ-45コンソールケーブル（[YRC-RJ45C](https://network.yamaha.com/products/options/yrc-rj45c/index)）
- USBシリアル変換ケーブル（FT232Rチップ搭載機を使用）
# ケーブルをつなぎ込む
コンソールケーブルと変換ケーブルで RJ-45⇔USB を作る
![console-usbcable.jpg](/img/user/img/Tech/console-usbcable.jpg)
USBをPCに接続しドライバが当たることを確認する
![usbcerealport.png](/img/user/img/Tech/usbcerealport.png)
最後にRJ-45をRTX1210のCONSOLEポートに接続する
# Tera Term で接続する
デバイスマネージャーで確認したCOMポート番号と同じインターフェースを選択して「OK」を押下する
![teraterm-comport.png](/img/user/img/Tech/teraterm-comport.png)

Enterを挟んで `Password:` が表示されたらパスワードを入力してログインする
![teraterm-rtx1210login.png](/img/user/img/Tech/teraterm-rtx1210login.png)
適当なコマンドを入力して、COMSOLEポート経由で対話できることを確認する
（例：`show environment`）![teraterm-rtx1210-env.png](/img/user/img/Tech/teraterm-rtx1210-env.png)


> [!caution]
> 日本語が文字化けする場合がある
> この場合 Tera Term の設定を変更することで解消できる
![teraterm-rtx1210-jpbake.png](/img/user/img/Tech/teraterm-rtx1210-jpbake.png)
  エンコーディング > Encodeing > SJIS（CP932）
![teraterm-cp932.png](/img/user/img/Tech/teraterm-cp932.png)