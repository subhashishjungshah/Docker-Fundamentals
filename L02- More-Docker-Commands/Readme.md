# Lesson 2 

Type the following Docker commands:

## Pull and run a Nginx server

    docker run -d -p 8080:80 --name webserver nginx
    - This command pulls a nginx image from web and names it as webserver. It opens the port 8080:80 in our local host. `-d` flag specifies a detached mode meaning,the container will run in background and returns the container ID. `-p` specifies a port enable port for our nginx server to run.

## List the running containers

    docker ps
    - This command lists all the containers running. We can use additional flag `-a` to check all the containers in memory.

## List the images

    docker images
    - This command lists all the images present in our local machine. For this example, we pulled nginx. This will show nginx in our local machine.

## Attach to the container

    docker container exec -it  webserver bash  
    - This command takes us inside the webserver's terminal. Once we execute this command, we are inside nginx bash terminal and can execute different scripts.

Exit by typing

    exit
    - To come out from ngnix bash terminal, we can use exit command.

## Stop the container

    docker stop webserver
    - Docker stop webserver stops our running webserver container. But it will be still inside our memory

## Remove the container from memory

    docker rm webserver
    - To delete the container from memory, we can use this command. `rm` stands for remove and webserver is our container's name.

## Remove the image

    docker rmi nginx
    - This command deletes nginx image from our local machine. Normally images are cache inside our local machine and consumes memory if we dont remove them. We can use this command to remove images from our local.