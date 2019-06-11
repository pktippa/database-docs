# Users

## Creating a superuser

```psql
create role temp with superuser;
```

## Listing out all the users

```psql
\du
```

## Giving login permissions / attributes

```psql
alter role temp with login;
```

## Adding to postgres group

```psql
grant postgres to temp;
```

## Setting up password

```psql
\password temp;
```

## Verifying the new superuser

```psql
postgres=# \du
                                    List of roles
 Role name |                         Attributes                         | Member of
-----------+------------------------------------------------------------+------------
 postgres  | Superuser, Create role, Create DB, Replication, Bypass RLS | {}
 temp      | Superuser                                                  | {postgres}
```
