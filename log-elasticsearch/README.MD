docker run -v /log-elasticsearch:/data --name log-pd registry.eztable.com/log-elasticsearch echo "data-only container for log-elasticsearch"

docker run --volumes-from log-pd -p 9200:9200 -p 9300:9300 -d --name log-elasticsearch registry.eztable.com/log-elasticsearch
