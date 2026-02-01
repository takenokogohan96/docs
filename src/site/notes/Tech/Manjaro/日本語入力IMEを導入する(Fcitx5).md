---
{"dg-publish":true,"dg-permalink":"manjaro-install-fcitx5","permalink":"/manjaro-install-fcitx5/","created":"2026-01-13T08:19:40.000+09:00","updated":"2026-02-01T14:18:15.399+09:00"}
---

## Fictx5本体を導入する
```
sudo pacman -S manjaro-asian-input-support-fcitx5
```

Gnome環境の場合、加えてGnome拡張 [Input Method Panel](https://extensions.gnome.org/extension/261/kimpanel/) を入れる
- 変換候補のポップアップ表示位置を入力入力と被らせない
- IMEの状態(MozcなJP⇔US など)をトップバーに表示する
## カタカナ英語の変換
[カナ英辞書v2.txt](https://www.mediafire.com/?cy1mxpjds5l5h)を辞書ツールに導入する![fcitx5-kana-english.png](/img/user/img/Tech/fcitx5-kana-english.png)