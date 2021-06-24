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



