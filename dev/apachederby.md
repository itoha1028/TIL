---
tags:
  - derby
  - datebase
---

# Derby実装メモ

## Derby

derbyは設定ファイル

プロパティの各項目にはスコープが存在する。 それぞれ、以下のスコープとなる。 System-wide Property：システム全体に掛かる Database-wide Property：データベース単体に掛かる

[https://db.apache.org/derby/docs/10.9/ref/crefproper22250.html](https://db.apache.org/derby/docs/10.9/ref/crefproper22250.html)

それぞれのプロパティの設定方法は以下に記載されている。 [https://db.apache.org/derby/docs/10.5/devguide/index.html](https://db.apache.org/derby/docs/10.5/devguide/index.html) \(v10.5の例\)

