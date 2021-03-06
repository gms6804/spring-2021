# This Tutorial Builds the Bioconductor_docker image with Asciinema functionality

In this tutorial, we use a [bioconductor docker images](https://hub.docker.com/r/bioconductor/bioconductor_docker) that includes [asciinema](https://asciinema.org/) functionality.

In the examples below, `$` indicates the command line prompt within the container.

## 1) create asccinema.org account

## 2) open docker terminal

## 3) pull container
```
docker pull bioconductor/bioconductor_docker
```

## 4) boot into container as bash
```
docker run -it bioconductor/bioconductor_docker bash
```

## 5) Installing asciinema # https://asciinema.org/docs/installation
```
$ apt-get update
$ apt-get install asciinema
[ctrl-p] # exit container
```

## 6) Commit, tag and save to Dockerhub
```
docker container ls
docker commit [CONTAINER ID] dominicklemas/bioconductor_asciinema
docker tag [IMAGE ID] dominicklemas/bioconductor_asciinema:02_2020
docker login
docker push dominicklemas/bioconductor_asciinema:02_2020
```