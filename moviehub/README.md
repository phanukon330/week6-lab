# MovieHub

## Local database and movie preview

The preview command uses `DATABASE_URL` when set. Otherwise, it connects to
the local development database on `127.0.0.1:5433`.

The SQL dump must be available at `../moviehub_dump.sql` relative to this
directory. Start PostgreSQL and load the dump on first initialization:

```sh
docker compose up -d --wait
go run ./cmd/peek
```

Search for a title:

```sh
go run ./cmd/peek -q "movie title"
```

To connect to a different database, set `DATABASE_URL`. The local development
database credentials are for local use only; do not use them in production.
