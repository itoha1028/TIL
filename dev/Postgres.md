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

## テーブル毎のデータ容量を取得する
```
SELECT relname, reltuples as rows, (relpages * cast(8192 as bigint)) as bytes FROM pg_class;
```


## 最初の1件を取得する
OFFSET 0 LIMIT 1;

## 
```
SELECT relname, n_live_tup, n_dead_tup, last_vacuum, last_autovacuum, last_analyze, last_autoanalyze FROM pg_stat_all_tables WHERE schemaname = 'scm_adpf_op' ORDER BY relname;
```

## 
SELECT datname, age(datfrozenxid) FROM pg_database;

## ストアドプロシージャの一覧を表示する
```
SELECT p.proname FROM pg_catalog.pg_namespace n JOIN pg_catalog.pg_proc p ON p.pronamespace = n.oid WHERE  n.nspname = '<スキーマ名>';
```

## ストアドプロシージャーの処理を表示する
```
SELECT proname, prosrc FROM pg_catalog.pg_namespace n JOIN pg_catalog.pg_proc p ON pronamespace = n.oid WHERE  proname = '<プロシージャー名>';
```