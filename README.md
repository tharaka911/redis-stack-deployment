### install docker

### make directory
```sh
cd /var/lib/docker/volumes && mkdir redis-data
```
### Make file and copy the configurations
```sh
cd /var/lib/docker/volumes/redis-data && nano local-redis-stack.conf
```
### Alter the below for password change
```
#defult user
requirepass add_root_password_here
#custom user
user add_user_here on +@all ~* &* +subscribe >add_user_password_here
```
### deploy docker container
```sh
docker run -d -v /var/lib/docker/volumes/redis-data/local-redis-stack.conf:/redis-stack.conf -v /var/lib/docker/volumes/redis-data:/data -p 6380:6379 -p 8002:8001 redis/redis-stack:latest
```
