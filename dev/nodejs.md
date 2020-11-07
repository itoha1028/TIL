---
tags:
  - nodejs
  - javascript
---

# 環境構築編

## バージョン管理環境の構築

nodeのパッケージマネージャであるnodenvを使用する

1. 以下を参考に構

   [nodenv を使って Mac に Node.js の環境を構築する](https://qiita.com/1000ch/items/41ea7caffe8c42c5211c)

## 新しいバージョンのインストール

```bash
$ nodenv install xx.xx.xx
```

最新のバージョンは [nodejs公式](https://nodejs.org/ja/download/)から確認

## プロジェクト毎にバージョンを指定

1. バージョン指定

   ```bash
    $ nodenv local xx.xx.xx
   ```

2. プロジェクトのディレクトリ配下に、`.node-version`というバージョンの記載されたファイルが作成される

