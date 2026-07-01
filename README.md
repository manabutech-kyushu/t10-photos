# t10-photos

Slack SCIM プロフィール写真の公開ホスティング用。
Slack が anonymous に画像 URL を fetch するため public にしている。

## 使い方

`photos/<key>.<ext>` を配置して push すると、以下の raw URL で参照できる:

```
https://raw.githubusercontent.com/manabutech-kyushu/t10-photos/main/photos/<key>.<ext>
```

これを Slack SCIM の `photos[].value` に指定する。

## 対象

t10-sync-team-members スキル (`.claude/skills/t10-sync-team-members/`) 経由で
Salesforce デモ用 Slack org のプロフィール写真として使う。
実在の SE の顔写真は上げない (架空人物のみ)。
