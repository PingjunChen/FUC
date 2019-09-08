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

:code:`$ docker build -t <image_name>:[tag_name] .`

Save image

:code:`$ docker save <image_name>:[tag_name] <image_name>.tar`

Load image

:code:`$ docker load --input <image_name>.tar`

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

:code:`$ docker run -it --restart always --name <container_name> <image_name>:[tag_name]`

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


Nvidia-Docker
--------

Install nvidia-docker 2.0

.. code-block:: bash

    $ curl -s -L https://nvidia.github.io/nvidia-docker/gpgkey | sudo apt-key add -
    $ distribution=$(. /etc/os-release;echo $ID$VERSION_ID)
    $ curl -s -L https://nvidia.github.io/nvidia-docker/$distribution/nvidia-docker.list | \
        sudo tee /etc/apt/sources.list.d/nvidia-docker.list
    $ sudo apt-get update
    $ sudo apt-get install nvidia-docker2
    $ sudo pkill -SIGHUP dockerd
    $ docker run --runtime nvidia --rm nvidia/cuda:9.0-base-ubuntu16.04 nvidia-smi
