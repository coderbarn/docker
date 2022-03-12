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


<br><br>

[sampleDocker](sampleDocker/README.md)<br>
[sampleDockerCompose](sampleDockerCompose/README.md)


## Diagnosing problems

1. From DockerDesktop [Here](https://docs.docker.com/desktop/mac/troubleshoot/)
2. From CLI use the com.docker.diagnose tool probably located here: <font color=green>/Applications/Docker.app/Contents/MacOS/comdocker.diagnose</font>

To create and upload diagnostics, run:

 /Applications/Docker.app/Contents/MacOS/com.docker.diagnose gather -upload

 After the diagnostics have finished, you should have the following output, containing your diagnostics ID:
<br> <font color=green>
Diagnostics Bundle: /tmp/B8CF8400-47B3-4068-ADA4-3BBDCE3985D9/20190726143610.zip<br>
Diagnostics ID:     B8CF8400-47B3-4068-ADA4-3BBDCE3985D9/20190726143610 (uploaded)<br>
Diagnostics Bundle: /tmp/BE9AFAAF-F68B-41D0-9D12-84760E6B8740/20190905152051.zip<br>
Diagnostics ID:     BE9AFAAF-F68B-41D0-9D12-84760E6B8740/20190905152051 (uploaded)<br>
</font>
<br>