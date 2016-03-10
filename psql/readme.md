### Connect as root

```console
$ sudo -u postgres psql
```

### Create new user
```console
postgres=# CREATE USER example WITH PASSWORD 'example';
```

##### Change user Password
```console
postgres=# ALTER USER username WITH LOGIN PASSWORD 'new_password';
```

### Grant the user
```console
postgres=# GRANT ALL PRIVILEGES ON DATABASE example to example;
```

### Add extensions
postgis is used as example

```console
postgres=# CREATE EXTENSION IF NOT EXISTS postgis;
```

### Make an SQL dump
```console
$ pg_dump -c -O -x --if-exists dbname > dump_$(date -Iseconds).sql
```

Bonus. You can define this function in your `.zshrc` (or directly from the shell):

```bash
function pg_dump_to_file {
    sudo -u postgres pg_dump -c -O -x --if-exists $1 > $1_$(date -Iseconds).sql
}
```

Then simply call it

```console
$ pg_dump_to_file my_db_name
```

### Inject an SQL Dump to an existing DB
```console
$ psql your_db_name < /path/to/dump.sql
```

### Postgres URL format
use the following template in every Django projects `postgres://username:password@hostname/db_name`

To quit just type `\q`
