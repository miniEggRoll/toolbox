## how to start
docker run --name proxy --net=host --env-file nginx/env.list -v ~/nginx:/tmp/volume -d registry.eztable.com/nginx-proxy


## dir_to_mount
- docker-registry.htpasswd
- certs/docker-registry
- private/docker-registry
- certs/eztable.com.chained.crt
- private/eztable_wildcard.key
