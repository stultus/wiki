---
description: >-
  Docker is a set of platform as a service (PaaS) products that use OS-level
  virtualization to deliver software in packages called containers.
---

# Docker

### Setup

#### Install docker edge release on your Linux machine. 

```text
curl -sSL https://get.docker.com/ | sh
```

[store.docker.com](https://store.docker.com) has instruction for each distro if you want to install docker on a production environment. 

#### Add your user to docker group

```text
sudo usermod -aG docker <user-username>
```

#### Install `docker-machine` and `docker-compose` 

* Follow the [official documentation](https://docs.docker.com/machine/install-machine/) to install docker machine
* Follow the [official documentation](https://docs.docker.com/compose/install/) to install docker compose

### Image vs. Container

* An image is the application we want to run - the binaries, libraries and the source code that all make up your application - packaged 
* A container is a running instance of that image 
* We can have many containers running off the same image
* registries are the image repositories. Docker's default image registry is at [Docker Hub](https://hub.docker.com)

####  Example usage to run `nginx` container 

```text
docker container run --publish 80:80 nginx
```

The above command did the following things 

* Downloaded the image '`nginx`' from Docker hub \(as the image was not available locally\)
* Started a new container from that image
* Opened port 80 on the host IP and started routing all host port 80 traffic to the container IP, port 80

The following command will do all the above things, but it will do it in the background. 

```text
docker container run --publish 80:80 --detatch nginx
```

Use the following command to list the containers 

```text
docker container ls
```

the above command only lists the currently running containers.  use `ls -a` to get a list of all the containers

Use the following command to stop a container \(which is running in the background\)

```text
docker container stop <container id>
```

And the following command will show the logs from a container

```text
docker container logs <container name>
```

