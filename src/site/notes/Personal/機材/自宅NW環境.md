---
{"dg-publish":true,"dg-permalink":"home-network","permalink":"/home-network/","created":"2026-01-26T14:14:54.321+09:00","updated":"2026-01-26T14:19:21.998+09:00"}
---

- 主回線と予備回線の2回線、主回線はIPoEとPPPoE併用運用につき合計3回線
- YAMAHA RTXシリーズを中心にNW機器はヤマハ製中心
- 写真中央は[[Personal/機材/自作Xeonサーバ機\|自作Xeonサーバ機]]、その他殆ど全ての機器をスチールラックに収容
![homerack.jpg](/img/user/img/Personal/homerack.jpg)

## 物理構成図
- シンプルにルータとAPを繋いでいるだけ
- RTX1210 の LAN1 は ポートベースVLANで半々に切り出す
![nw-wiring.png](/img/user/img/Personal/nw-wiring.png)
## 論理構成図
- 予備回線と主回線のクライアントセグメントは特にひねりなし
- サーバセグメントは原則 Cloudflare Tunnel を以ってLAN外に公開
- PPPoE接続で払い出されるIPv4アドレスをゲートセグメントで扱う
![nw-logic.png](/img/user/img/Personal/nw-logic.png)
