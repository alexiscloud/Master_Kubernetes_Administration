# Running container
Type the following Docker commands:

## Pull and run a Nginx server

    docker run -d -p 8080:80 --name webserver nginx

> Pull and run a Nginx server

<img src="https://github.com/alexiscloud/Master_Kubernetes_Administration/blob/main/Screenshot 2023-05-25 112216.jpg?raw=true" width ="100%">
## List the running containers

    docker ps

## List the images

    docker images

## Attach to the container

    docker container exec -it  webserver bash  

Exit by typing

    exit

## Stop the container

    docker stop webserver

## Remove the container from memory

    docker rm webserver

## Remove the image

    docker rmi nginx