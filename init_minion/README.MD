Adjust params and exec create

In create, it would
- create minion boot disk with snapshot
- create docker persistent disk
- create VM instance with startup script

In startup script, it would 
- setup salt-master ip and minion id
- start salt-minion daemon
- sync files by state.highstate
- update registry certificate and restart docker

After exec create, you should 
- echo "UUID={UUID of disk} /var/lib/docker ext4 defaults 1 1” >> /etc/fstab
- mount -a

