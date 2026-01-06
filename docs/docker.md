# Various useful Docker commands

* docker ps
* docker container ls
* docker image ls
* docker exec -it <container name> sh 			<-- interactive terminal running shell
* ctrl-p ctrl-q 					<-- exit running container, leave it running in daemon mode

* docker logs <container name>				<-- syslog and more
* docker rm <container name> 				<-- remove container
* docker stop <container name> 				<-- stop running container 
* docker builder prune					<-- clear docker cache

## Remote private repository (currently broken)
* docker tag busybox 192.168.128.75:6088/admin/busybox	<-- tag local image for repository
* docker push 192.168.128.75:6088/admin/busybox 		<-- push to private repository
* curl -k -u admin:[passwd] https://192.168.128.75:6088/v2/_catalog
* docker login -u admin 192.168.128.75:6088		<-- login to repository to be able to push/pull!
[URL to instructions](https://medium.com/@yaroslavberkut/how-i-spun-up-custom-docker-registry-on-my-own-qnap-server-490f87e30167)

## Build / run images
* docker build -t pambot:latest . && docker run -it --name run-pambot -p 8000:8000 pambot:latest
* docker run --name pam_mongo -p 27017:27017 -d mongo:4.2.18

## Build containers from command line (semi-automated):
* ~/docker_containers/buildPush.sh
* cd ~/docker_containers/pam_stack
* docker pull mongo-express:latest
* docker stack deploy pam_stack --compose-file docker-compose.yml
* docker compose up

## Docker compose
* docker compose up
* docker compose stop
* docker compose ls
