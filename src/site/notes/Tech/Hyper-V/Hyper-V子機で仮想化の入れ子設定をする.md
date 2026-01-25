---
{"dg-publish":true,"dg-permalink":"hyperv-nested-virtualization","permalink":"/hyperv-nested-virtualization/","created":"2026-01-25T15:14:44.660+09:00","updated":"2026-01-18T02:26:52.223+09:00"}
---

Hyper-V子機で Docker Desktop をインストール後起動した際に以下のエラーが表示される場合がある
![hyperv-neserror.png](/img/user/img/Tech/hyperv-neserror.png)
この場合「Hyper-V仮想化の入れ子設定」が必要になる
1. VMをシャットダウンしてホストOSに戻る
2. 以下のコマンドを投入する
```
Set-VMProcessor –{仮想マシンの名前} -ExposeVirtualizationExtensions $true
```