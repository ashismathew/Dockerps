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


Ashiss-MBP:e2e Ashis$ ./network_setup.sh down
setting to default channel 'mychannel'
WARNING: The ARCH_TAG variable is not set. Defaulting to a blank string.
WARNING: The CHANNEL_NAME variable is not set. Defaulting to a blank string.
Removing network e2e_default
WARNING: Network e2e_default not found.
138776dc3cfb
85e432d3921d
07b275028dd7
8ed38a95e01a
6cf7acedd6c7
1b72ea992fd0
Untagged: dev-peer0-digitalproperty-network-0.7.2:latest
Deleted: sha256:6dcce89e16238eb170acd0d7f2e01fdc17d810cf51f885f24023ed17dfa87870
Deleted: sha256:177e9665951a8d0fb1b09eefd1b104354a9f42dce17c0be506ecb9d77611e270
Deleted: sha256:d087f24b58b0e04288721c994e46f4a8148ca9634dd21c09c2d44a77b955b8fc
Untagged: dev-peer1-digitalproperty-network-0.7.2:latest
Deleted: sha256:f83878d5b6825f73812e42b64218cf9e3ed493c60ac48b23b1244f4c22edc62d
Deleted: sha256:c6a9ec727230c542271765773bb65f98ff8f4afad86c4f0a7a368b6b5f15a0dd
Deleted: sha256:6df9f9ebba27ef8fd5df689298eeb49191d739f607bb6786f474eb792838b9b2


Install Node.js and NPM
http://blog.teamtreehouse.com/install-node-js-npm-mac


Hyperledger Composer
=====================

git clone https://github.com/hyperledger/composer-sample-applications-hlfv1.git

shiss-MBP:getting-started Ashis$ pwd
/Users/Ashis/hyperledger/composer-sample-applications-hlfv1/packages/getting-started

Ashiss-MBP:getting-started Ashis$ npm install


Ashiss-MBP:getting-started Ashis$ npm test

Hyperledger Composer Playground
================================
Ashiss-MBP:getting-started Ashis$ pwd
/Users/Ashis/hyperledger/composer-sample-applications-hlfv1/packages/getting-started

Ashiss-MBP:getting-started Ashis$ npm install -g composer-playground

Ashiss-MBP:getting-started Ashis$ docker-composer playground

http://localhost:8080


Generating a REST API
=======================

API will be dynamically generated by Loopback..

Install the general purpose Composer REST Server
====================
npm install -g composer-rest-server

composer-rest-server -p h1fv1 -n digital-property-network -i admin -s adminpw -N always
Ashiss-MBP:hlfv1 Ashis$ pwd
/Users/Ashis/.composer-connection-profiles/hlfv1


| | | |  _   _   _ __     ___   _ __  | |   ___    __| |   __ _    ___   _ __           / ___|   ___    _ __ ___    _ __     ___    ___    ___   _ __ 
 | |_| | | | | | | '_ \   / _ \ | '__| | |  / _ \  / _` |  / _` |  / _ \ | '__|  _____  | |      / _ \  | '_ ` _ \  | '_ \   / _ \  / __|  / _ \ | '__|
 |  _  | | |_| | | |_) | |  __/ | |    | | |  __/ | (_| | | (_| | |  __/ | |    |_____| | |___  | (_) | | | | | | | | |_) | | (_) | \__ \ |  __/ | |   
 |_| |_|  \__, | | .__/   \___| |_|    |_|  \___|  \__,_|  \__, |  \___| |_|             \____|  \___/  |_| |_| |_| | .__/   \___/  |___/  \___| |_|   
          |___/  |_|                                       |___/                                                    |_|                                
? Enter your Fabric Connection Profile Name: hlfv1
? Enter your Business Network Identifier : digitalproperty-network
? Enter your Fabric username : admin
? Enter your secret: adminpw
? Specify if you want namespaces in the generated REST API: always use namespaces
? Specify if you want the generated REST API to be secured: No

To restart the REST server using the same options, issue the following command:
   composer-rest-server -p hlfv1 -n digitalproperty-network -i admin -s adminpw -N always

Discovering types from business network definition ...
Discovered types from business network definition
Generating schemas for all types in business network definition ...
Generated schemas for all types in business network definition
Adding schemas for all types to Loopback ...
{ name: 'net_biz_digitalPropertyNetwork_LandTitle',
  description: 'An asset named LandTitle',
  plural: 'net.biz.digitalPropertyNetwork.LandTitle',
  base: 'PersistedModel',
  idInjection: false,
  options: 
   { validateUpsert: true,
     composer: 
      { type: 'asset',
        namespace: 'net.biz.digitalPropertyNetwork',
        name: 'LandTitle',

relations: {},
  acls: 
   [ { accessType: '*',
       permission: 'ALLOW',
       principalId: '$authenticated',
       principalType: 'ROLE' },
     { accessType: '*',
       permission: 'DENY',
       principalId: '$unauthenticated',
       principalType: 'ROLE' } ],
  methods: [],
  forceId: true }
Added schemas for all types to Loopback
Web server listening at: http://localhost:3000
Browse your REST API at http://localhost:3000/explorer


composer-rest-server -p hlfv1 -n digitalproperty-network -i admin -s adminpw -N always

composer archive create --sourceName digitalproperty-network --sourceType module --archiveFile digitalPropertyNetwork.bna

Ashiss-MBP:getting-started Ashis$ composer archive create --sourceName digitalproperty-network --sourceType module --archiveFile digitalPropertyNetwork.bna

Creating Business Network Archive

Node module search path : 
undefined 

Not found in main node_module search path, trying current directory :/Users/Ashis/hyperledger/composer-sample-applications-hlfv1/packages/getting-started/node_modules/digitalproperty-network
Looking for package.json of Business Network Definition in /Users/Ashis/hyperledger/composer-sample-applications-hlfv1/packages/getting-started/node_modules/digitalproperty-network

Found:
Description:Digital Property Network
Name:digitalproperty-network
Identifier:digitalproperty-network@0.0.7

Written Business Network Definition Archive file to digitalPropertyNetwork.bna
Command completed successfully.

Command succeeded




