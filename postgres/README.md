# Postgres

## Database Related

[Database](database.md)

## PgSql

[PGSql](pgsql.md)

## SQLs

### DB creation

```sql
CREATE DATABASE database_name
  WITH OWNER = postgres
       ENCODING = 'UTF8'
       TABLESPACE = pg_default
       LC_COLLATE = 'English_India.1252'
       LC_CTYPE = 'English_India.1252'
       CONNECTION LIMIT = -1;
	   
```

### Table Creation

Here we have auto increment

```sql
CREATE TABLE public.table_name
(
  id integer NOT NULL DEFAULT nextval('table_name_id_seq'::regclass),
  data text,
  CONSTRAINT table_name_pkey PRIMARY KEY (id)
)
WITH (
  OIDS=FALSE
);
ALTER TABLE public.table_name
  OWNER TO postgres;
```

### Deleting records

```sql
DELETE from  public.table_name;
```

