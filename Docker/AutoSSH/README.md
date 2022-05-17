The Docker file builds a docker image which allows the user to automatically perform a ssh login on a Ubuntu docker host 

**Instruction to build the docker image**
1. docker build -t autossh --build-arg hostname=ubuntu-12 --build-arg username=freddy --build-arg release=`lsb_release -c | sed s/Codename://g | sed -e   s/[[:space:]]//g`  -f Dockerfile

**Instruction to run the docker container**
  2. docker run -t autossh 
