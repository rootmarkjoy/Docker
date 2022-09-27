# Docker

Docker Documentation URL: https://docs.docker.com/


# Docker_Commands

- Obtain the container ID by running the following command: docker ps

- Access the Docker container by running the following command: docker exec -it <container_id> /bin/bash

e.g
----
Container login command:-
docker exec -it 6466 /bin/bash

- container_id
Is the ID of the container obtained with the command explained in the first step, for example 6466b9201126.

- To list all the containers you have made:
sudo docker ps -a

- And select the container you want to work with (mine is 0f19152b7a14):
sudo docker start -ai 0f19152b7a14
