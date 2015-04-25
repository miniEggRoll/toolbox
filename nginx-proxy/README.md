## how to start
docker run --name proxy --net=host --env-file nginx/env.list -v ~/nginx:/tmp/volume -d registry.eztable.com/nginx-proxy
