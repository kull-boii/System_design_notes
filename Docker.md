If your system is also used for building images you might have a look at cleaning up garbage created by the builders using:

you can view all the caches by navigating to linux > docker-desktop-data > docker > overlay2

`docker buildx prune --all`

`docker builder prune --all`

deletes all docker image cache.

<br>

To inspect env of a container `docker inspect <container_name>`

to get continious logs `docker logs -f <container_name>`

The docker cp is a handy command but a lesser-known one. It is used to copy files/folders between a container and the host’s local file system. One use-case I have used recently is to copy the node_modules from the container in the build phase in the CI pipeline and reuse it in the test phase on the host. It easily saved 30+ seconds of npm install time. Below are a couple of examples to copy a file from host to container and vice versa.


docker container IP address
`docker inspect <container_name>` or 
`docker container inspect --format "{{ .NetworkSettings.IPAddress }}" <container_name>`



### addons
- https://geshan.com.np/blog/2022/05/docker-commands/
