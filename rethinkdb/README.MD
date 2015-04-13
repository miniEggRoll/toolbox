#persistent disk

docker run -v /pd:/data —name rethinkdb-pd dockerfile/ubuntu echo "data-only container for rethinkdb"

#rethinkdb

docker run —volumes-from rethinkdb-pd —name rerthinkdb -p 28015:28015 -p 29015:29015 -p 8080:8080 dockerfile/rethinkdb
