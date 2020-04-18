# Docker Commands
 
**It is a containerization platform that combines all our application in package. So it runs in any environment.**
 
_For more detail [Docker Page](https://www.docker.com)_

_[Learn docker](https://training.play-with-docker.com)_

## To verify docker is installed or not run
 ```$ docker --version```

## List all **running** containers
  ```$ docker ps```  
  **OR**  <br>
  ```#docker container ls```

## List all container which are in **created** or **exited** state
  ```$ docker ps -a``` 
  **OR**  <br>
  ```# docker container ls -a```

## Pull docker image from docker hub (registry)
  ```$ docker image pull <image-name>```

  _eg:_
  ```$ docker image pull alpine```

  _alpine is a lightweight linux distribution_


## To list all the images
  ```$ docker image ls```

## To run a container
  ```$ docker container run <image-name>```

  _eg:_
   ```
    $ docker container run hello-world`
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
1. _Now we are creating a file inside alpine container_<br>
  ```$ docker container run -it alpine /bin/ash```

  _/bin/ash is a type of shell in alpine_ <br>
  `-it is a flag for interactice terminal`

  - _After that command you will see something like this_ `/ #` _this is a prompt of /bin/ash shell, run some basic  commands of linux like ls, cd, .._

  - _Now create a file inside this container and name it as iso.txt_
  - _Then type_ `exit`

  - _run_ `docker container ls -a` _, then copy the Container-ID of latest alpine container in a editor or somewhere else._

2. Viewing the file
  _Follow the below steps:_
  ```
    $ docker container run -it alpine /bin/ash
    / # ls 
  ```

  _Yup, It does not display the file that we have created Right?_

  _Open a new terminal and run the following command:_

  ```
   $ docker container start <paste-here-container-id>
  ```

  _List the running containers_

  ```
    $ docker container ls 
  ```
   _Run ls command on that container_

  ```
    $ docker container exec <container-id> ls
  ```
  _Here you will definately see the file that we have created._

  **This is called as container isolation. When you run a image, it creates a new container(say object).**<br>
  **So each container has a seperate filesystem. When we create a file in a container and exited that. It is in stop state.**<br>
  **Again we instantiated a new container(say object), it is a different from previous container.**<br>
  **Like in java, let say we have created a class Bicycle. Then we are instantiating two objects of a bicycle. So these two are different from each other. The one does not know what other do and vice-versa.**<br>
  **In a docker this is called a container isolation.**<br>
  **For understanding say image as a class and container as a object.**<br>


## Stop the running container
 ```
  $ docker stop <container-id>
 ```
 **run** `docker ps` **command and copy the container id**


 ```
  $ docker stop <conatiner-name>
 ```

## Start the container
 ```
  $ docker start <container-id>
 ```
 **run** `docker ps -a` **command and copy the container id**