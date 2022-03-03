

1)	Pull any image from dockerhub ( image name is redis in this case)

docker pull redis

2)	Run container from any image from dockerhub ( image name is hello-world in this case )

docker run hello-world

3)	Display list of all docker images

docker images

4)	Run container in detached mode and mapped to certain port

docker run -d -p 8600:8080 pengbai/docker-supermario

5)	Display currently running containers

docker ps

6)	Display all the containers ( running + stopped )

docker ps -a

7)	Stop the running container 

docker stop <container_id>

8)	Remove the stopped container 

docker rm <container_id>

9)	Remove the running container ( To remove the running container, either you need to stop it and remove OR you need to force removal )

docker rm -f <container_id> 

10)	Remove docker image ( Before removing image make sure we have removed container associated with it )

docker rmi redis

11)	To remove all the containers forcibly in single command

docker rm -f $(docker ps -aq)

12)	To remove all the images in single command ( -f for forcing )

docker rmi $(docker images -q) 

13)	Export Images to tar file and Import images from tar file. ( Backup Activities )

docker pull redis
docker pull nginx
docker images

Command to export images in tar file
docker save redis nginx -o images.tar

docker rmi redis
docker rmi nginx
docker images

Command to import images from tar file
docker load -i images.tar



