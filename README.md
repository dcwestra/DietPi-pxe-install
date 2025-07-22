# DietPi-pxe-install
Custom ipxe menu that will automatically install DietPi over the network

## How to set up
1) Configure NetBoot.xyz
  - See the docs here: https://netboot.xyz/docs/category/docker-container
  - Watch this video from TechnoTim: https://youtu.be/4btW5x_clpg?si=ymwRZofAMd-qIQr0
  - I included a sample docker-compose.yml with optional traefik config
  - Don't forget to update your router for network booting
2) Create a directory for NetBoot.xyz assets
3) Create a NFS share with the assets directory
  - it may be helpful to open the share on a computer with a desktop for some of the following steps
4) Create a directory for Dietpi within the assets folder
5) Download and extract the desired DietPi image: https://dietpi.com/#downloadinfo
6) Mount the image and copy the contents into the DietPi folder
7) Bind mount the assets directory to /assets in Netboot.xyz
8) Visit the Web UI for Netboot.xyz at http://ip-of-host:3000 or the FQDN set up in Trafeik
9) Set up the dietpi.ipxe as a new menu entry
10) Modify linux.ipxe to include an entry for DietPi - you can also replace with the linux.ipxe in this repo

Now you should be able to pxe boot into NetBoot.xyz
Select Linux Network Installs and select DietPi from the list
DietPi should start installing automatically.
