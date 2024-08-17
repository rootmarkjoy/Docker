Docker Process Management
-------------------------

Show all running docker containers
```sh
$ docker ps
```

Show all docker containers
```sh
$ docker ps -a
```

Run a container
```sh
$ docker run <image>:<tag>
```

Run a container and connect to it
```sh
$ docker run -it <image>:<tag>
```

Run a container and clean it up after exit
```sh
$ docker run --rm <image>:<tag>
```

Run a container in the background
```sh
$ docker run -d <image>:<tag>
```

Stop a container
```sh
$ docker stop <container>
```

Kill a container
```sh
$ docker kill <container>
```


### Docker Images and Repositories
------------------------------

List available local images
```sh
$ docker image ls
```

Search for docker images
```sh
$ docker search <image>
```

Pull a docker image
```sh
$ docker image pull <image>
```

Build an image with a dockerfile
```sh
$ docker image build -t <image>:<tag> <run_directory> -f <dockerfile>
```

Login to a remote repository
```sh
$ docker login <repository>
```

Push an image to your remotee repository
```sh
$ docker image push <image>:<tag>
```

Remove a local docker image
```sh
$ docker image rm <image>:<tag>
```

Show metadata for an image
```sh
$ docker image inspect <image>
```

Remove all unused docker images
```sh
$ docker image prune
```


### Docker Volumes and Ports
------------------------

List volumes
```sh
$ docker volume ls
```

Create a volume
```sh
$ docker volume create <volume>
```

Delete a volume
```sh
$ docker volume rm <volume>
```

Show volume metadata
```sh
$ docker volume inspect <volume>
```

Delete all volumes not attached to a container
```sh
$ docker volume prune
```

Mount a local directory to your container
```sh
$ docker run -v <local_dir>:<container_dir> <image>
```

Copy file or folder from a docker container to host machine
```sh
$ docker cp <container>:<container_dir> <local_dir>
```

Copy file or folder from local machine onto a container
```sh
$ docker cp <local_dir> <container>:<container_dir>
```

Map a local port to a docker instance
```sh
$ docker run -d -p 127.0.0.1:<local_port>:<docker_port> <image>
```

List the ports a docker container is running on
```sh
$ docker port <container>
```


### Docker Troubleshooting
----------------------

Show the logs of a container
```sh
$ docker logs <container>
```

Follow/tail the logs of a container
```sh
$ docker logs -f <container>
```

Show timestamps on docker logs
```sh
$ docker logs -t <container>
```

Show details/metadata of a container
```sh
$ docker inspect <container>
```

Show a 'top' view of processes running on a container
```sh
$ docker top <container>
```

Show a 'top' view of all docker containers
```sh
$ docker stats
```

Show any files that have changed since startup
```sh
$ docker diff <container>
```

Connect to an already running container
```sh
$ docker attach <container>
```

Execute a command on a container
```sh
$ docker exec -it <container_id> /bin/bash
```

Show docker system wide information
```sh
$ docker system info
```

Show docker disk space used
```sh
$ docker system df
```


### Docker Compose
--------------

Start your docker-compose defined resources in detached mode
```sh
$ docker-compose up -d -f <docker_compose_yaml>
```

Stop all docker-compose resources
```sh
$ docker-compose stop
```

Destroy all docker-compose resources
```sh
$ docker-compose down
```

Show docker-compose processes
```sh
$ docker-compose ps
```

Show docker-compose logs
```sh
$ docker-compose logs
```

Show docker-compose resource consumption
```sh
$ docker-compose top
```

Pull latest docker-compose images
```sh
$ docker-compose pull
```

