# Docker MySQL

## Quick Start

```bash
docker run --name mysql -d cedvan/mysql:latest
```

## User and Database

```bash
docker run --name mysql -d \
    -e 'DB_USER=dbuser' \
    -e 'DB_PASS=dbpass' \
    -e 'DB_NAME=dbname' \
    cedvan/mysql:latest
```

## Multiple databases

```bash
docker run --name mysql -d \
    -e 'DB_NAME=dbname1, dbname2' \
    cedvan/mysql:latest
```

## Save Data

```bash
docker run --name mysql -d \
    -v /opt/mysql/data:/var/lib/mysql \
    cedvan/mysql:latest
```