# I am watching "ELEC4630 Online Tuto-s1-full"

container img

container can use root, if it breaks, we can always open a new one.


a container inside a container?

What is dev container?

Go can run cmd in a program. So go can set up a container.

This tut doesnot use docker, instead realize container or docker in a lower level, it creats isolate process ID, Name env, file sys. This means it realize the bisic things all the containers do.


# Use docker

We can use a exit image.

https://hub.docker.com/_/ubuntu

or we can build a new image based on a parent image.

https://docs.docker.com/build/building/base-images/


`docker container run --rm --name onion myjupyter`   --rm Automatically remove the container when it exits

`docker build --rm -t myjupyter .` --rm Remove intermediate containers 


`docker ps -a`
`docker rm onion`
`docker image prune`

## copy file into docker

dockerfile format in <https://docs.docker.com/reference/dockerfile/>\

COPY ./SimpleFingerprintRecognitionExample /home/jovyan/work

## import into docker

## run container

`docker container run -m 2GB --user root -e CHOWN_HOME=yes -e CHOWN_HOME_OPTS='-R' -d --name onion myjupyter` add run paras to fix permission problem

## use github in docker

RUN apt-get -y install git
RUN git clone https://github.com/shizhan1109/ELEC4630.git
