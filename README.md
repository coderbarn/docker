# docker

Examples on how to build and run docker containers

### General docker commands

- docker system info
- docker system events
- docker system df
- docker system prune

Space is only freed when images are deleted. Space is not freed automatically when files are deleted inside running containers. To trigger a space reclamation at any point, run the command

<font color=green>
 > docker run --privileged --pid=host docker/desktop-reclaim-space
</font>

[sampleDocker](sampleDocker/README.md)
[sampleDockerCompose](sampleDockerCompose/README.md)
