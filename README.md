# docker

1. to build: docker build --tag python-docker .
2. to ssh into container
3. docker exec -it <name of the conatiner> /bin/bash
4. docker exec -it compassionate_robinson /bin/bash

- docker images
- docker run python-docker
- docker run --publish 9880:80 python-docker
- docker ps
- docker rmi 783234ab3