---
{"dg-publish":true,"dg-permalink":"rtx1210-firmwareupdate","permalink":"/rtx1210-firmwareupdate/","created":"2026-01-25T15:14:45.628+09:00","updated":"2026-01-18T00:52:24.350+09:00"}
---


> [!caution] 
> あらかじめ対象機が「「RTX1210」 不具合対策プログラム」の対象か確認を行う
> https://network.yamaha.com/support/rtx1210_boot

# 現在のファームフェアバージョンを確認

```
show environment
```

上から4行目くらいに現在のファームフェアバージョンが表示
```
RTX1210 Rev.14.01.40 (Fri Apr 16 09:27:57 2021)
```

[ヤマハネットワーク周辺機器 リリースノート](https://www.rtpro.yamaha.co.jp/RT/docs/relnote/index.html) によると確認時最新は Rev.14 系列 の **Rev.14.01.42**
# ファームウェアをアップデートする
1. [ファームウェア配布ページ](https://www.rtpro.yamaha.co.jp/RT/firmware/index.php) から当該機のファームウェアをダウンロードする
2. WebGUI > 管理 > 保守 > ファームウェアの更新 > PCからファームウェアを更新 と遷移する
3. 「更新ファイルの指定」を、DLした `rtx1210.bin` に指定する
4. 入力内容の確認画面で「実行」を押下する
5. 更新ファイルの確認 → 更新 → 再起動と自動的に進行する
6. LEDの点滅終了後に「トップへ戻る」ボタンを押下し、再びログインする
7. バージョンを確認する

```
RTX1210 Rev.14.01.42 (Fri Jul  5 11:17:45 2024)
```