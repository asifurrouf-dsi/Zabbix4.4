# Docker Frequently Used Commands #

## Docker Compose ##

1. docker-compose up || docker-compose up -d || docker-compose down
2. docker-compose ps
3. docker-compose stop || docker-compose start
4. docker-compose rm -f

## Docker Logs ##

1. docker logs containerID

## Docker Containers ##

1. docker run --rm -ti -d -e DISPLAY=x.x.x.x:0 -v /path/to/mount:/mount/point/in/container -p hostPort:containerPort imageID
2. docker run --rm -ti -p 1313:1313 -v $(pwd):/srv/hugo hugo sh
3. docker ps -a

To drop out of interactive session on container: <ctrl-p><ctrl-q>
https://docs.docker.com/engine/quickstart/#running-an-interactive-shell
NOTE: this does not seem to work with Docker Beta for Mac on "docker run", but does work for "docker exec"

4. docker stop containerID
5. docker start  containerID

NOTE: may need to remove 'attach' from this list 
6. docker attach containerID

http://stackoverflow.com/questions/30960686/difference-between-docker-attach-and-docker-exec
https://forums.docker.com/t/exec-vs-attach-commands/4210

7. docker exec -ti containerID /bin/bash
8. docker logs containerID

$ docker help logs

Usage:	docker logs [OPTIONS] CONTAINER

Fetch the logs of a container

  -f, --follow        Follow log output
  --help              Print usage
  --since             Show logs since timestamp
  -t, --timestamps    Show timestamps
  --tail=all          Number of lines to show from the end of the logs


9. docker rm containerID

## Docker Images ##

1. docker images
2. docker rmi imageID
3. docker build -t containerName (assumes that valid `Dockerfile` exists in the current directory)

## Docker Registry ##

1. docker login
2. docker pull
3. docker push



