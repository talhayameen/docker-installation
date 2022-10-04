# docker-installation
This repo is for installing docker offline in linux

#1- CLone this repo
git clone https://github.com/talhayameen/docker-installation.git

#2 goto folder docker-installation
cd docker-installation

#3 Either you can unpackage each file of .deb OR you can unpackage all at once.

Note: Use sudo with dpkg command so that docker will be installed in root directory with proper rights.

sudo dpkg -i containerd.io_1.4.9-1_amd64.deb
sudo dpkg -i docker-ce_20.10.8_3-0_ubuntu-focal_amd64.deb
sudo dpkg -i docker-ce-cli_20.10.8_3-0_ubuntu-focal_amd64.deb

OR unpack all by one command

sudo dpkg -i *.deb

Now docker has been installed , You can check,

docker -v

Now time to install docker-compose

#4 Copy docker-compose file to /usr/local/bin/
cp docker-compose /usr/local/bin/

#5 Give executeable permissions to docker-compose file 
sudo chmod +x /usr/local/bin/docker-compose

Now docker-compose has been installed , You can check,
docker-compose -v
