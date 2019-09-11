# 1. Scale docker image storage

1. `sudo service docker stop`
2. `sudo mv /var/lib/docker /thenewlocation`
3. Edit the /etc/default/docker file, inserting/Modifing
	`DOCKER_OPTS="-g /thenewlocation/docker"`
4. `sudo service docker start`

# 2. Fix Bug: cyber_recorder can not find share library

`source cyber/setup.bash`
`cd /usr/lib/x86_64-linux-gnu`
`ln -s libboost_signals.so.1.65.1 libboost_signals.so.1.54.0`
`ln -s libboost_thread.so.1.65.1 libboost_thread.so.1.54.0`
`ln -s libboost_system.so.1.65.1 libboost_system.so.1.54.0`
`cd /apollo`

