#nsqlookupd

docker run --name nsqlookupd -p 4161:4161 -p 4160:4160 nsqio/nsqlookupd


# nsqd

docker run -v /pd/nsqd:/data --name nsqd-pd nsqio/nsq echo "data-only container for nsqd"

docker run --volumes-from nsqd-pd -p 4151:4151 -p 4150:5150 --name nsqd nsqio/nsqd --broadcast-address=daemon-ip --lookupd-tcp-address=lookupd-ip:4160


# admin

docker run -d -p 4171:4171 --name nsq-admin nsqio/nsqadmin --lookupd-http-address=lookupd-ip:4161
