# seeds

Create SQL files under `seeds/default` and write INSERT statements as shown below.

```sql
INSERT INTO public.todo (id, body) values (1, 'write a blog post'), (2, 'jog');
```

Then run the following command inside `hasura-console`` container to execute all SQL files.

```sh
docker-compose exec hasura-console bash
```

```sh
hasura seed apply
```

If you want to execute only a specific SQL file, run the following command.

```sh
hasura seed apply --file reset_all.sql
```

See official documentation for more details.

- https://hasura.io/docs/latest/hasura-cli/commands/hasura_seed_apply/

# migrations

See official documentation for more details.

- https://hasura.io/docs/latest/hasura-cli/commands/hasura_migrate_create/
- https://hasura.io/docs/latest/hasura-cli/commands/hasura_migrate_apply/
