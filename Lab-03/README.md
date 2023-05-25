# Running container
Type the following Docker commands:

## Pull and run a Nginx server

    docker run -d -p 8080:80 --name webserver nginx

> Pull and run a Nginx server

<img src="https://github.com/alexiscloud/Master_Kubernetes_Administration/blob/main/Screenshots/Screenshot 2023-05-25 112216.jpg?raw=true" width ="80%">
## List the running containers

    docker ps
> List the running container
<img src="https://github.com/alexiscloud/Master_Kubernetes_Administration/blob/main/Screenshots/Screenshot 2023-05-25 112309.jpg?raw=true" width ="80%">
## List the images

    docker images

> list the images
<img src="https://github.com/alexiscloud/Master_Kubernetes_Administration/blob/main/Screenshots/Screenshot 2023-05-25 112337.jpg?raw=true" width ="80%">
## Attach to the container

    docker container exec -it  webserver bash  


> attach to the contaner
<img src="https://github.com/alexiscloud/Master_Kubernetes_Administration/blob/main/Screenshots/Screenshot 2023-05-25 112441.jpg?raw=true" width ="80%">
Exit by typing

    exit

## Stop the container

    docker stop webserver

## Remove the container from memory

    docker rm webserver

## Remove the image

    docker rmi nginx

> stop ,rm ,rmi
<img src="https://github.com/alexiscloud/Master_Kubernetes_Administration/blob/main/Screenshots/Screenshot 2023-05-25 112610.jpg?raw=true" width ="80%">