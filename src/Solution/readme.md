# Commands to execute
## How to build a docker container?
EXEC on any shell you have/prefer: 'docker build -t "javaservice:v2" .'

## How to run a docker container?
EXEC on any shell you have/prefer: docker run -p 8095:8090 -it --restart always javaservice:v2

## How to attach to a already running container?
EXEC on any shell you have/prefer: docker attach [docker-container-ID]