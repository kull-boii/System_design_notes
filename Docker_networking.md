- https://www.freecodecamp.org/news/how-to-get-a-docker-container-ip-address-explained-with-examples/
<br>



**Why is virtualization required for Docker?**

To run Docker Desktop in a virtual desktop environment, it is essential nested virtualization is enabled on the virtual machine that provides the virtual desktop. This is because, under the hood, Docker Desktop is using a Linux VM in which it runs Docker Engine and the containers.

<img width="859" alt="mobyvm" src="https://user-images.githubusercontent.com/68529036/206181508-7c47b1d8-a965-4ea7-8c9e-7e7593367f49.png">


In windows
- type ipconfig/all
- run docker desktop
- type ipconfig/all (you will see a new network: WSL
- run three docker containers
- docker run -itd --rm --name d1 nginx
- docker run -itd --rm --name d2 nginx
- docker run -itd --rm --name d3 nginx
- type docker network ls
- copy the network id of bridge
- docker network inspect <network_id_copied>
- notice three container ip address and gateway address
- Addons: notice "com.docker.network.bridge.name": "docker0", at the end
- ![image](https://user-images.githubusercontent.com/68529036/206182771-4892077d-b8d8-48f4-bd34-97792047dfac.png)
- docker0 is new virtual bridge interface (default interface and network for the default bidge, the defualt network in docker
