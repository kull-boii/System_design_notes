### You can use aws and launch multiple ec2 instances (node1: n1,n2,n3...)

`docker swarm init --advertise-addr` <manager-ip (host public ip)>`  This command intializes a swarm with a manager


it outputs a join token to add any worker and to add a manager just type `docker swarm join-token manager`

to view all the nodes `docker node ls`

if a worker node needs to be removed we can type `docker swarm leave --force` in worker node

to remove a node from the manager type `docker node rm <node_id>`

no need to save the token we can get it anytime just type `docker swarm join-token worker(or manager)`

suppose you have 3 ec2 instances (1 manager 2 workers) and we want to launch nginx container on each one of them

`docker service create --name new-service --replicas 3 -p 80:80 nginx`

`docker service rm <service_name>`

to inspect a service

`docker service inspect --pretty <service_name>`

`docker service ps <service_name>`
