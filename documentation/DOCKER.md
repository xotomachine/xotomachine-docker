- [HOW TO USE THIS IMAGE](#how-to-use-this-image)
- [GET STARTED WITH NVIM](#get-started-with-nvim)
- [OTHER USEFUL COMMANDS](#other-useful-commands)

## HOW TO USE THIS IMAGE

```shell
docker-compose build --no-cache && docker run -it --rm xotomachine-docker_machine # build and run
docker login # login to docker hub
docker push gregcousin126/xotomachine-docker # push to docker hub
cd /home docker run --rm -it -v $PWD:/xotomachine gregcousin126/xotomachine-docker:latest # run machine
```

<hr>

## GET STARTED WITH NVIM

``` shell
# RUN THE FOLLOWING
nvim # run the editor and hit shift + :
# TYPE : PACKER
```

<hr>

## OTHER USEFUL COMMANDS

``` shell
sudo service docker restart
docker container ls # check all containers and its status
docker exec -it container_id /bin/bash # enter in the shell or bash of a particular container
docker stop $(docker ps -a -q) # stop all containers
docker rm -f $(docker ps -a -q) # delete all containers
docker volume rm $(docker volume ls -q) # delete all volumes
docker rmi -f $(sudo docker images -q) # delete all container images
```
