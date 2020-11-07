---
tags:
  - git
---

# 誤ってpushしてしまったファイルをgit管理の歴史上から抹消する

## 全てのブランチから削除する

```text
git filter-branch --tree-filter 'rm -f common/key/id_rsa' HEAD --all
```

## 参照ログから削除する

```text
git reflog expire --expire=now --all
```

## リポジトリを掃除する

```text
git gc --aggressive --prune=now
```

## 抹消する

```text
git push --force origin master
```

