---
tags:
  - git
---

# 誤ってpushしてしまったファイルをgit管理の歴史上から抹消する

## 全てのブランチから削除する
```
git filter-branch --tree-filter 'rm -f common/key/id_rsa' HEAD --all
```

## 参照ログから削除する
```
git reflog expire --expire=now --all
```

## リポジトリを掃除する
```
git gc --aggressive --prune=now
```

## 抹消する
```
git push --force origin master
```