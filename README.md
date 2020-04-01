# Docker Commands
 
**It is a containerization platform that combines all our application in package. So it runs in any environment.**
 
**For more detail [Docker Page](https://www.docker.com)**

## To verify docker is installed or not run
 ```# docker --version```

## List all **running** containers
 ```# docker ps```  **OR**  ```#docker container ls```

## List all container which are in **created** or **exited** state
 ```# docker ps -a```  **OR**  ```# docker container ls -a```

## To run a container
 ```# docker container run <container-name>```

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
