## postgresql server
```
docker run --name rod6.postgres -e POSTGRES_PASSWORD=wothing -e POSTGRES_USER=wothing -e PGDATA=/db -v /Users/rod/Develop/db:/db -d postgres
```

## postgresql client
```
docker run -it --link rod6.postgres:postgres --rm postgres sh -c 'exec psql -h postgres -p 5432 -U wothing'
```

## consul
```
docker run -d --name=rod6.consul consul
```

## redis server
```
docker run --name rod6.redis -d redis:alpine
```

## redis client
```
docker run -it --link rod6.redis:redis --rm redis:alpine redis-cli -h redis -p 6379
```
