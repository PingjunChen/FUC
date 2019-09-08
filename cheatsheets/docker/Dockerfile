FROM nvidia/cuda:9.0-base-ubuntu16.04

MAINTAINER chenpingjun <chenpingjun@gmx.com>

RUN apt-get update && apt-get install -y --no-install-recommends \
	build-essential curl sudo git
 && rm -rf /var/lib/apt/lists/*

# Create a non-root user and switch to it
ARG USER_NAME="chenpingjun"
RUN adduser --disabled-password --gecos '' --shell /bin/bash ${USER_NAME}
RUN echo "${USER_NAME} ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/90-${USER_NAME}
USER ${USER_NAME}
ENV HOME=/home/${USER_NAME}
RUN chmod 777 /home/${USER_NAME}
WORKDIR /home/${USER_NAME}

# Install Miniconda
RUN curl -so ~/miniconda.sh https://repo.continuum.io/miniconda/Miniconda3-4.5.11-Linux-x86_64.sh \
 && chmod +x ~/miniconda.sh \
 && ~/miniconda.sh -b -p ~/miniconda \
 && rm ~/miniconda.sh
ENV PATH=/home/${USER_NAME}/miniconda/bin:$PATH
ENV CONDA_AUTO_UPDATE_CONDA=false

# Create a Python 3.6 environment
RUN /home/${USER_NAME}/miniconda/bin/conda install conda-build \
 && /home/${USER_NAME}/miniconda/bin/conda create -y --name py36 python=3.6.5 \
 && /home/${USER_NAME}/miniconda/bin/conda clean -ya
ENV CONDA_DEFAULT_ENV=py36
ENV CONDA_PREFIX=/home/${USER_NAME}/miniconda/envs/$CONDA_DEFAULT_ENV
ENV PATH=$CONDA_PREFIX/bin:$PATH

# CUDA 9.0-specific steps
RUN conda install -y -c pytorch cuda90=1.0 magma-cuda90=2.4.0 \
    "pytorch=1.0.0=py3.6_cuda9.0.176_cudnn7.4.1_1" \
    torchvision=0.2.1 \
 && conda clean -ya
