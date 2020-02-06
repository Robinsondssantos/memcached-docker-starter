# Docker starter postgresql

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

## Start a postgresql instance
```
user@computer:~$ docker run --name database-name -e POSTGRES_PASSWORD=my-secret-password -p 5432:5432 -d postgres
```

## Check if postgresql was running
```
user@computer:~$ docker ps
```

## Check all containers 
```
user@computer:~$ docker ps -aq
```

## Restart a postgresql instance
```
user@computer:~$ docker restart <postgresql_container>
```
