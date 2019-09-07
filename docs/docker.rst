docker
========

`Docker <https://www.docker.com/>`_ is an open platform for developers and
sysadmins to build, ship, and run distributed applications, whether on laptops,
data center VMs, or the cloud.


Docker Installation
--------

Install docker

:code:`$ sudo apt install docker.io`

Add user to docker group

:code:`$ sudo usermod -aG docker $USER`


Image management
--------

Create **image** from `Dockerfile <https://docs.docker.com/engine/reference/builder/>`_

:code:`$ docker build -t <image_name> <Dockerfile_dir>`

List available images

:code:`$ docker images`

Remove image by name

:code:`$ docker rmi <image_name>`

Remove image by id

:code:`$ docker rmi <image_id>`


Remove dangling images

:code:`$ docker images purge`


Container management
--------

Start container

:code:`$ docker run --name <container_name> --restart always --shm-size 12G -it -p 8888:8888 -v ~/Downloads/:/Coding <image_name>`

List container

:code:`$ docker ps`

Remove container

:code:`$ docker stop <container_name>`

:code:`$ docker rm <container_name>`

Upload image to docker hub
--------

Set docker hub username

:code:`$ export DOCKER_ID_USER="user_name"`

Login in to docker hub

:code:`$ docker login`

Tag image

:code:`$ docker tag <image_name> $DOCKER_ID_USER/<image_name>`

Push to docker cloud

:code:`$ docker push $DOCKER_ID_USER/<image_name>`
