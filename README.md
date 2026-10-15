# week6-lab

## MovieHub preview

From the repository root, start the local MovieHub database, list movies, or
run the API:

```sh
docker compose -f moviehub/docker-compose.yml up -d --wait
go run ./moviehub/cmd/peek
go run ./moviehub
```

The API uses `moviehub/.jwt_secret` for local development when `JWT_SECRET` is
not set. Set `DATABASE_URL` and `JWT_SECRET` to override local defaults.

Search by title:

```sh
go run ./moviehub/cmd/peek -q "Spider"
```
