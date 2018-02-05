# MongoDB

## Import and Export

Exporting

```sh
$ mongoexport /db:db_name /collection:collection_name /out:"path/to/file.json" /jsonArray /pretty
$ # for more run `mongoexport --help`
```

Importing

```sh
$ mongoimport /db:db_name /collection:collection_name /file:"path/to/file.json" /jsonArray /maintainInsertionOrder
$ # for more run `mongoimport --help`
```
