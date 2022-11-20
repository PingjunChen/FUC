docker
========
`Docker <https://www.docker.com/>`_ is an open platform for developers and
sysadmins to build, ship, and run distributed applications, whether on laptops,
data center VMs, or the cloud.


Docker Installation
--------

.. code-block:: bash

    $ sudo apt install docker.io        # install docker
    $ sudo usermod -aG docker $USER     # add user to docker group


Image management
--------

Create **image** from `Dockerfile <https://docs.docker.com/engine/reference/builder/>`_

:code:`$ docker build -t <image_name>:[tag_name] .`

Create **image** from a specific Dockerfile

:code:`$ docker build -f <dockerfile_name> -t <image_name>:[tag_name] .`

Image management

.. code-block:: bash

    $ docker save <image_name>:[tag_name] <image_name>.tar      # save image
    $ docker load --input <image_name>.tar                      # load image
    $ docker images                                             # list available images
    $ docker rmi <image_name>                                   # remove image by name
    $ docker rmi <image_id>                                     # remove image by id
    $ docker images purge                                       # remove dangling images


Container management
--------

Start container

.. code-block:: bash

    $ docker run -it --restart always --name <container_name> <image_name>:[tag_name]
    Options:
        -v <local_dir>:<docker_dir>:ro            # map local directory to docker
        --runtime=nvidia                          # expose NVIDIA GPUs
        -e NVIDIA_VISIBLE_DEVICES=5               # cuda device setting
        --shm-size 16G                            # set size of shared memory
        --rm                                      # remove container file system when exits


Copy files

.. code-block:: bash

    $ docker cp <container_name>:<src_dir> <local_dst_dir>  # copy files from docker to local
    $ docker cp <local_src_dir> <container_name>:<dst_dir>  # copy files from local to docker

Container management

.. code-block:: bash

    $ docker ps                         # list all available containers
    $ docker stop <container_name>      # stop specific container
    $ docker rm <container_name>        # remove specific stopped container

Upload image to docker hub
--------

Login to docker hub

.. code-block:: bash

    $ export DOCKER_ID_USER="user_name"   # set docker hub username
    $ docker login                        # login in to docker hub

Tag image

:code:`$ docker tag <image_name>:<version> $DOCKER_ID_USER/<image_name>:<version>`

Push to docker cloud

:code:`$ docker push $DOCKER_ID_USER/<image_name>:<version>`


Convert image to singularity
--------

Create docker image tarball

.. code-block:: bash

    $ docker save <image_name>:<version> -o <image_name>.tar

Build singularity from image tarball

.. code-block:: bash

    $ singularity build <image_name>.sif docker-archive://<image_name>.tar

Build singularity from DockerHub image

.. code-block:: bash

    $ singularity pull <image_name>.sif docker://<user_name>/<image_name>:<version>


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
