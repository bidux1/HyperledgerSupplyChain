
In case you haven’t downloaded the education repository for this course, follow the below directions in your terminal window:


$ cd HyperledgerSupplyChain/LFS171x/fabric-material/tuna-app

Make sure you have Docker running on your machine before you run the next command. If you do not have Docker installed, return to Chapter 4, Technical Requirements.

Also, make sure that you have completed the Installing Hyperledger Fabric section in this chapter before moving on to this application section, as you will likely experience errors. 

First, remove any pre-existing containers, as it may conflict with commands in this tutorial:

$ docker rm -f $(docker ps -aq)

Then, let’s start the Hyperledger Fabric network with the following command:

$ ./startFabric.sh

 

Troubleshooting: If, after running the above you are getting an error similar to the following:

ERROR: failed to register layer: rename
/var/lib/docker/image/overlay2/layerdb/tmp/write-set-091347846 /var/lib/docker/image/overlay2/layerdb/sha256/9d3227c1793b7494e598caafd0a5013900e17dcdf1d7bdd31d39c82be04fcf28: file exists

try running the following command:

$ rm -rf ~/Library/Containers/com.docker.docker/Data/*

$ npm install

$ node registerAdmin.js

$ node registerUser.js

$ node server.js
Troubleshooting: If you are getting an error similar to the one below while attempting to perform any of the functions on the application:

Error: [client-utils.js]: sendPeersProposal - Promise is rejected: Error: Connect Failed

error from query =  { Error: Connect Failed

   at /Desktop/prj/education/LFS171x/fabric-material/tuna-app/node_modules/grpc/src/node/src/client.js:554:15 code: 14, metadata: Metadata { _internal_repr: {} } }

try running the following commands:

$ cd ~

$ rm -rf .hfc-key-store/

Then, run the commands above starting with:

$ node registerAdmin.js