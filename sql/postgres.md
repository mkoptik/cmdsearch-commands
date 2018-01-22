# PostgreSQL commands

### Backup database with pg_dump

```
pg_dump --host <hostname> --port 5432 --format tar --blobs --verbose --file <output-file> --username <username> -W <database-name>
```

### Restore database with pg_restore

```
pg_restore -U <username> -d <database-name> < <backup-file>
```

## PostgreSQL in Docker

### Start in docker with custom configuration

```
docker run -d --name <container-name> postgres -c 'shared_buffers=256MB' -c 'max_connections=200'
```

### Open psql in docker container as postgres user

```
docker exec -it -u postgres <container-name> psql
```

### Execute SQL file in docker container via psql as postgres user

```
docker exec -i <container-name> psql -U postgres -d <database-name> -W < <file-name-on-host-machine>
```