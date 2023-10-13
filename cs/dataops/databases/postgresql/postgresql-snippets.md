# PostgreSQL Snippets

## See Postgres locks

```sql
SELECT t.relname, l.locktype, page, virtualtransaction, pid, mode, granted 
FROM pg_locks l, pg_stat_all_tables t 
WHERE l.relation = t.relid ORDER BY relation asc;
```



## Select 10 most largest Postgres tables

```sql
select schemaname as table_schema,
    relname as table_name,
    pg_size_pretty(pg_total_relation_size(relid)) as total_size,
    pg_size_pretty(pg_relation_size(relid)) as data_size,
    pg_size_pretty(pg_total_relation_size(relid) - pg_relation_size(relid))
      as external_size
from pg_catalog.pg_statio_user_tables
order by pg_total_relation_size(relid) desc,
         pg_relation_size(relid) desc
limit 10;
```



## Blocking Sessions

```sql
SELECT 
	pl.pid as blocked_pid
	,psa.usename as blocked_user
	,pl2.pid as blocking_pid
	,psa2.usename as blocking_user
	,psa.query as blocked_statement
FROM pg_catalog.pg_locks pl
JOIN pg_catalog.pg_stat_activity psa
	ON pl.pid = psa.pid
JOIN pg_catalog.pg_locks pl2
JOIN pg_catalog.pg_stat_activity psa2
	ON pl2.pid = psa2.pid
	ON pl.transactionid = pl2.transactionid 
		AND pl.pid != pl2.pid
WHERE NOT pl.granted;
```



## Transactions that are idle for 15 mins

```sql
SELECT
  pid,
  now() - pg_stat_activity.query_start AS duration,
  query,
  state
FROM pg_stat_activity
WHERE (now() - pg_stat_activity.query_start) > interval '15 minutes';
```



## Terminate transactions that are idle for 15 mins

```sql
SELECT pg_terminate_backend(pid)
FROM pg_stat_activity
WHERE datname = 'my_db'
	AND pid <> pg_backend_pid()
	AND state in ('idle', 'idle in transaction', 'idle in transaction (aborted)', 'disabled') 
	AND state_change < current_timestamp - INTERVAL '15' MINUTE;q
```
