# docker

1. to build: docker build --tag python-docker .
2. to ssh into container
3. docker exec -it <name of the conatiner> /bin/bash
4. docker exec -it compassionate_robinson /bin/bash
5. An alternate sudo docker attach compassionate_robinson

- docker build . -t flasktestapp 
- docker run python-docker
- docker run --publish 9880:80 python-docker
- docker run --publish 9880:80 --name mydockertest -d python-docker
- docker ps
- docker ps -a // Lists all containers
- docker images
- docker rmi 783234ab3
- docker container ls -a // view all containers
- docker container prune // removes all stopped containers