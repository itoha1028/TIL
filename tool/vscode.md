---
tags:
  - vscode
  - editor
---
# Vosual Studio Code
## 任意のショートカットを定義する
1. コマンドパレッドを開く<br>
`Cmd+Shift+p`

1. "Open Keyboard Shortcuts(JSON)"を選択する

1. リストにショートカットを追加する<br>
例えばマークダウンファイルの場合に `Cmd+Enter` で`<br>`タグを入力したい場合の設定は以下のようになる。
```
{"key": "Cmd+enter", "command": "type", "args": {"text": "<br>"}, "when": "editorTextFocus && editorLangId == 'markdown'"}
```

