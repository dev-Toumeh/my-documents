## build and run 

### from hub/remote without changes (the image should exist in docker.hub)
- docker pull image-name
- docker run -it --name my-container-name -d image-name

## from local Dockerfile
- docker build -t image-name /path/to/dockerfile 
- docker run -it --name my-container -d image-name

## start the container if it was created 
- docker start my-container

## To list all Docker containers that use the same image
docker ps -a --filter ancestor=your_image_name --format "{{.ID}}" | xargs docker rm
