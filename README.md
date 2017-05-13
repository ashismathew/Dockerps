# Dockerps
#stop and remove all container
 #Adding the -a flag will show all containers. 
 #When you're sure you want to delete them, you can add the -q flag to supply the IDs to the docker stop and docker rm commands:

docker rm $(docker ps -a -q)

#Removing images according to a pattern
docker ps -a |  grep "pattern"

#Remove all images with force option
docker rmi -f $(docker images -a -q)

