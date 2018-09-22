# Docker CheatSheet

### Create image from Dockerfile
```
docker build -t <image_name> <Dockerfile_parent_dir>   # create image from Dockerfile 

```

### Images
```
$ docker images                          # list available images
$ docker rmi <image_name> or <image_id>  # remove certain image
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
