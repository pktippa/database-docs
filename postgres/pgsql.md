# PSQL

Connecting to database

```sh
psql -U postgres -d database_name
```

## Internal commands

### Listing all the functions

```psql
# -- regex is for name of function also.
# \df <regex>;
```

### To view the source code of existing custom function

```psql
# -- dont add semicolon at the end
# \sf <function_name>
```
