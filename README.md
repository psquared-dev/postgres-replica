Create replication user:

`create user repuser replication;`

To create replica directory

`sudo pg_basebackup -h localhost -p 5432 -U repuser -D /tmp/secondary-postgres/ -Fp -Xs -R`

Check the loaded config file:

`SHOW hba_file;`

`SHOW config_file;`           


Check for connection:

`select * from pg_stat_replication;`