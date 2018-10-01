# Docker CheatSheet

### Create image from [Dockerfile](docker/Dockerfile.yaml)
```
docker build -t <image_name> <Dockerfile_parent_dir>   # create image from Dockerfile

```

### Image management
```
$ docker images                          # list available images
$ docker rmi <image_name> or <image_id>  # remove certain image
$ docker images purge                    # remove dangling images
```

### Start container
```
$ docker run --name <container_name> --restart always --shm-size 12G -it
  -p 8888:8888 -p 6006:6006
  -v ~/Downloads/:/Coding <image_name>                       # Run container from image
$ jupyter notebook --ip 0.0.0.0 --no-browser --allow-root    # Run jupyter in container to allow host to visit  
```

### Remove a container
```
$ docker ps                          # list all running containers
$ docker stop <container_name>       # stop specific container
$ docker rm <container_name>         # remove specific container
```


### Upload docker image to docker hub
```
$ export DOCKER_ID_USER="<user_name>"                    # set docker hub username
$ docker login                                           # login to docker hub
$ docker tag <image_name> $DOCKER_ID_USER/<image_name>   # tag the image
$ docker push $DOCKER_ID_USER/<image_name>               # push to docker cloud
```
