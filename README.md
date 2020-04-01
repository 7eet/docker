# Docker Commands
 
**It is a containerization platform that combines all our application in package. So it runs in any environment.**
 
_For more detail [Docker Page](https://www.docker.com)_

_[Learn docker](https://training.play-with-docker.com)_

## To verify docker is installed or not run
 ```# docker --version```

## List all **running** containers
 ```# docker ps```  **OR**  ```#docker container ls```

## List all container which are in **created** or **exited** state
 ```# docker ps -a```  **OR**  ```# docker container ls -a```

## Pull docker image from docker hub (registry)
 ```# docker image pull <image-name>```

_eg:_
 ```# docker image pull alpine```

_alpine is a lightweight linux distribution_


## To list all the images
 ```# docker image ls```

## To run a container
 ```# docker container run <image-name>```

_eg:_
 ```
  # docker container run hello-world`
  Hello from Docker!
  This message shows that your installation appears to be working correctly.

  To generate this message, Docker took the following steps:
   1. The Docker client contacted the Docker daemon.
   2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
      (amd64)
   3. The Docker daemon created a new container from that image which runs the
      executable that produces the output you are currently reading.
   4. The Docker daemon streamed that output to the Docker client, which sent it
      to your terminal.
 ```

## Inside the container
_Now we are creating a file inside alpine container_



