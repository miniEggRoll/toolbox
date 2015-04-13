docker run --name fluentd --env-file /srv/salt/docker/env/fluentd -d -v /var/lib/docker/containers:/var/lib/docker/containers -v /sys/fs/cgroups:/tmp/cgroup registry.eztable.com/fluentd
