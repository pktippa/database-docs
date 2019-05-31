# Postgres Database

Exporting database using `pg_dump`

```sh
pg_dump --dbname=db1 --host=localhost --port=5432 --username=postgres --file=postgre_database_dump.txt --role=postgres
```

The above command prompts for password.

Now restoring the database using `psql`

```sh
psql -U postgres -d db1 < postgre_database_dump.txt
```