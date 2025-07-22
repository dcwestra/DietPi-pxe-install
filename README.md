# DietPi-pxe-install
Custom ipxe menu that will automatically install DietPi over the network

## How to set up
1) Create a directory for NetBoot.xyz assets
2) Create a directory for Dietpi
3) Download and extract the desired DietPi image
4) Mount the image and copy the contents into the DietPi folder
5) Install Netboot.xyz in docker using the docker-compose.yml file
- Bind mount the assets directory to /assets in Netboot.xyz
6) Create a NFS share with the assets directory
7) to be continued after I get my wife ice cream.
