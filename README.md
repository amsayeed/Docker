![Docker General View](https://github.com/amsayeed/Docker/blob/main/docker.png?raw=true)
# Docker Fundamnetals
 Docker Course Repo

## Build simple hello world image
docker build -t hello-world .

## build fake user print image
docker build -f dockerfile-user -t hello-user .

## build image for repo and push
docker build -f dockerfile-user -t test/hello-user:latest .

docker push test/hello-user:latest


## remove image and pull new from repository
docker rmi test/my-repo:latest

docker pull test/my-repo:latest

## find and remove dangling images
docker images -f dangling=true

docker rmi -f $(docker images -f "dangling=true" -q)
