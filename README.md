# docker-cheat-sheet

## Clean up
* clean up any resources — images, containers, volumes, and networks
```
docker system prune
```
* remove any stopped containers and all unused images 
```
docker system prune -a
```
* list all docker images
```
docker images -a
```
* remove all docker images
```
docker rmi $(docker images -a -q)
```
* remove specific docker
```
docker rm docker_ID_or_Name docker_ID_or_Name
```
* remove all exited containers
```
docker rm $(docker ps -a -f status=exited -q)
```
* remove container according to pattern
```
docker ps -a | grep "pattern" | awk '{print $3}' | xargs docker rmi
```
* stop and remove all containers
```
docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)
```

