# Docker Container Configuration Cheat Sheet:

1.	--name: assigns a name to the container.
2.	--hostname: sets the hostname for the container.
3.	-e or --env: sets environment variables for the container.
4.	-p or --publish: publishes a container's port(s) to the host.
5.	--link: creates a link between two containers.
6.	--volumes-from: mounts volumes from another container.
7.	-v or --volume: mounts a host directory as a volume in the container.
8.	--net: sets the network mode for the container.
9.	--rm: automatically removes the container when it exits.
10.	-d or --detach: runs the container in detached mode.
11.	--memory: sets a memory limit for the container.
12.	--cpu-shares: sets the CPU shares for the container.
13.	--restart: specifies the restart policy for the container.
14.	--cap-add: adds Linux capabilities to the container.
15.	--cap-drop: drops Linux capabilities from the container.
Example:

```
docker run -d --name=my_web_server -p 80:80 -v /var/www:/web -e ENV=production --restart=always nginx
```
This example starts a new container named "my_web_server" running the nginx image in detached mode. 
It maps port 80 on the host to port 80 in the container, mounts the host directory /var/www to /web inside the container, 
sets the environment variable ENV to "production" and the container will be restarted always.