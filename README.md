```sh
docker run -d -v /var/lib/docker/volumes/redis-data/local-redis-stack.conf:/redis-stack.conf -v /var/lib/docker/volumes/redis-data:/data -p 6380:6379 -p 8002:8001 redis/redis-stack:latest
```
