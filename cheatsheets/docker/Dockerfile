FROM nvidia/cuda:10.2-base-ubuntu18.04

MAINTAINER pingjunchen <pingjunchen@ieee.org>

RUN apt-get update && apt-get install -y --no-install-recommends \
	build-essential curl sudo git wget python3-openslide \
 	&& rm -rf /var/lib/apt/lists/*

# Create a non-root user and switch to it
ARG USER_NAME="pingjun"
RUN adduser --disabled-password --gecos '' --shell /bin/bash ${USER_NAME}
RUN echo "${USER_NAME} ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/${USER_NAME}
USER ${USER_NAME}
ENV HOME=/home/${USER_NAME}
RUN chmod 777 /home/${USER_NAME}
WORKDIR /home/${USER_NAME}

# Install Miniconda
RUN curl -LO http://repo.continuum.io/miniconda/Miniconda3-py37_4.8.3-Linux-x86_64.sh \
 && bash ~/Miniconda3-py37_4.8.3-Linux-x86_64.sh -p ~/miniconda -b \
 && rm ~/Miniconda3-py37_4.8.3-Linux-x86_64.sh
ENV PATH=/home/${USER_NAME}/miniconda/bin:$PATH
ENV CONDA_AUTO_UPDATE_CONDA=false
## Create a Python 3.7 environment
RUN /home/${USER_NAME}/miniconda/bin/conda install conda-build \
 && /home/${USER_NAME}/miniconda/bin/conda create -y --name py37 python=3.7.5 \
 && /home/${USER_NAME}/miniconda/bin/conda clean -ya
ENV CONDA_DEFAULT_ENV=py37
ENV CONDA_PREFIX=/home/${USER_NAME}/miniconda/envs/$CONDA_DEFAULT_ENV
ENV PATH=$CONDA_PREFIX/bin:$PATH

# Python packages installation
## Using conda
RUN conda install -y ipython==7.16.1 \
	numpy==1.16.4 matplotlib==3.1.2 opencv==3.4.2
## Using pip
RUN pip install jupyter==1.0.0 setuptools==45
RUN pip install openslide-python==1.1.1
## Install pytorch
# RUN conda install pytorch torchvision cudatoolkit=10.2 -c pytorch
