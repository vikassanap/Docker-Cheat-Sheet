# Docker-Cheat-Sheet
Docker commands

#### Build Docker image from Dockerfile:
- `docker build -t imagename:tag .`

#### Pull Docker image:
- `docker pull imagename:tag`

#### List Docker images:
- `docker images`

#### Remove Docker image:
- `docker rmi -f imagename:tag`

#### Tag Docker image:
- `docker tag imagename:tag new_tag`

#### Run pulled Docker image:
- `docker run imagename:tag`

#### Run Docker image and enter into Docker container:
- `docker run -it imagename:tag bash`

#### List running Docker containers:
- `docker ps` 

#### Start Docker container with specific port mapped:
- `docker run -p host_port:container_port imagename:tag`

#### Start Docker container with any port mapped:
- `docker run -P imagename:tag`
- `docker ps => to see mapped port`

#### Name the Docker container:
- `docker run --name database imagename:tag`

#### Mount a folder inside container:
- `docker run -v host_folder:folder_inside_container imagename:tag`

#### Run container and exit after executing given command:
- `docker run imagename:tag <command to be executed>`

#### List stopped Docker containers:
- `docker ps -l`

#### Stop Docker container:
- `docker stop container_id`

#### Remove Docker container:
- `docker rm -f container_id`

#### Enter into running Docker container:
- `docker exec -it container_id bash`

#### Save Docker container as a Docker image:
- `docker commit container_id`
- `docker images`
- `docker tag image_id imagename:tag`

#### Push Docker image to Docker repo:
- `docker tag image_id <repo_url>:<tag>`
- `docker push <repo_url>:<tag>`

#### Delete all stopped and running containers:
- `docker rm -f $(docker ps -aq)`

#### See Docker container log:
- `docker logs container_id`
