---
tags:
  - ssl
  - web
---

# PSQL

# SQL
## 各テーブルのレコード数を取得する
```
SELECT T2.relname , T2.reltuples FROM pg_stat_user_tables AS T1 INNER JOIN pg_class AS T2 ON T1.relname = T2.relname ORDER BY T2.relname;
```

## 各テーブルのサイズを取得する
```
SELECT datname, pg_size_pretty(pg_database_size(datname)) FROM pg_database;
```