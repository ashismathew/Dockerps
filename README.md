# Dockerps
#stop and remove all container
 #Adding the -a flag will show all containers. 
 #When you're sure you want to delete them, you can add the -q flag to supply the IDs to the docker stop and docker rm commands:

docker rm $(docker ps -a -q)

#Removing images according to a pattern
docker ps -a |  grep "pattern"

#Remove all images with force option
docker rmi -f $(docker images -a -q)

Ashiss-MBP:e2e Ashis$ CHANNEL_NAME=channel_kutts docker-compose -f docker-compose-no-tls.yaml up -d
Creating network "e2e_default" with the default driver
Creating orderer.example.com
Creating peer0.org1.example.com
Creating peer1.org1.example.com
Creating peer0.org2.example.com
Creating peer1.org2.example.com
Creating cli
Ashiss-MBP:e2e Ashis$ pwd
/Users/Ashis/hyperledger/release/samples/e2e


$ ./network_setup.sh up

017-05-13 21:38:13.412 UTC [main] main -> INFO 006 Exiting.....
===================== Query on PEER3 on channel 'mychannel' is successful ===================== 

===================== All GOOD, End-2-End execution completed ===================== 




