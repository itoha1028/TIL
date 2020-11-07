---
tags:
  - vscode
  - editor
---

# Vosual Studio Code

## 任意のショートカットを定義する

1. コマンドパレッドを開く  `Cmd+Shift+p`
2. "Open Keyboard Shortcuts\(JSON\)"を選択する
3. リストにショートカットを追加する  
    例えばマークダウンファイルの場合に `Cmd+Enter` で`<br>`タグを入力したい場合の設定は以下のようになる。

   ```text
   {"key": "Cmd+enter", "command": "type", "args": {"text": "<br>"}, "when": "editorTextFocus && editorLangId == 'markdown'"}
   ```

