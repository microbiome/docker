
#README

#### This repo contains a _spiffy_ new docker container capable of running a [Bioconductor](https://github.com/Bioconductor/bioconductor_docker) base image of rstudio-server with mia and miaviz pre-installed and tailored for microbiome analyses!

#### In addition to all the stuff that the good folks at [Bioconductor](https://github.com/Bioconductor/bioconductor_docker) preinstalled into rstudio base image, we have pre-installed the following packages: \
`mia` \
`miaviz` \


## Simply launch the docker container and expose the port so you can enter it from a web browser by typing in the following commmand:

` docker run \
 	-e PASSWORD=bioc \
 	-p 8787:8787 \
 	jochum00/mia:1.0`


## This command will run the docker container `jochum00/mia:1.0` on your local machine. where RStudio will be available on your web browser at http://localhost:8787.


### Bioconductor base containers fix the username to always being rstudio. and the password in the above command is given as bioc but it can be set to anything.

### 8787 is the port being mapped between the docker container and your host machine. NOTE: password cannot be rstudio.

###  The user is logged into the rstudio user by default.

### Additional information regarding the use of bioconductor docker container based rstudio images can be found [here](https://github.com/Bioconductor/bioconductor_docker)


## Here is a link to the [Dockerhub](https://hub.docker.com/r/jochum00/mia)

## Alternatively you can build the container yourself using this [Dockerfile](https://github.com/microbiome/docker/blob/main/mia/Dockerfile)
