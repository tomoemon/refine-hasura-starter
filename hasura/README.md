Using the latest postgres database will cause inconsistencies with the client version installed on hasura's docker image, so increase the client version.

```
hasura migrate create init --from-server
```

```
FATA[0002] cannot fetch schema dump: pg_dump request: 500
{
  "error": "error while executing pg_dump",
  "path": "$",
  "code": "unexpected",
  "internal": "pg_dump: error: aborting because of server version mismatch\npg_dump: detail: server version: 16.1 (Debian 16.1-1.pgdg110+1); pg_dump version: 15.4 (Ubuntu 15.4-2.pgdg22.04+1)\n"
}
```
