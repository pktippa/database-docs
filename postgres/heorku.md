# Heroku Postgres

## Backup and restore

Taking dump and restore of postgres heroku database.

https://devcenter.heroku.com/articles/heroku-postgres-import-export

### Backup

Taking backup:

heroku pg:backups:capture --app heroku-app-name

Then download:
heroku pg:backups:download --app heroku-app-name

We get latest.dump, rename to current timestamp

### Restore

Convert into SQL file:
pg_restore -f db_dump.sql latest.dump

Change the owner name to 'postgres' by opening in any editor.

Then restore the dump file.

psql -U postgres -d database_name -f db_dump.sql
