If your system is also used for building images you might have a look at cleaning up garbage created by the builders using:

you can view all the caches by navigating to linux > docker-desktop-data > docker > overlay2

`docker buildx prune --all`

`docker builder prune --all`

deletes all docker image cache.
