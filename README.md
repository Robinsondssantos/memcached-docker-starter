# Memcached Docker starter

## Install docker in Ubuntu 19.04 (see how to install in your distro)
```
user@computer:~$ sudo snap install docker
```

## Check if docker was installed correctly
```
user@computer:~$ docker --version
Docker version 18.09.9, build 1752eb3
```

## if docker group does not exist, create it
```
user@computer:~$ sudo groupadd docker
```

## Add your user to the docker group
```
user@computer:~$ sudo usermod -aG docker $USER
```
*The user need to execute log in to see their new group added*

## Create the memcached container
```
user@computer:~$ docker run --name my-memcache -p 11211:11211 -d memcached memcached -m 64
```

## Check if memcached was running
```
user@computer:~$ docker ps -a
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                      NAMES
aed7986aec3a        memcached           "docker-entrypoint.s…"   16 minutes ago      Up 16 minutes       0.0.0.0:11211->11211/tcp   my-memcache
.
.
.
user@computer:~$
```

## Check all containers 
```
user@computer:~$ docker ps -a
```

## Start the memcached container
```
user@computer:~$ docker start <mecached_container_id>
```

## Show statistics of memcached container
```
user@computer:~$ docker stats <mecached_container_id>
```

## Restart a memcached container
```
user@computer:~$ docker restart <mecached_container_id>
```

## Remove a memcached container
```
user@computer:~$ docker rm <mecached_container_id>
```

