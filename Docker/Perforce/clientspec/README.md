The docker file builds a docker image which syncs user provided Perforce clientspec

1. Instruction to build the docker image 

docker build -t clientspec --build-arg --build-arg p4clientspec=myP4Client --build-arg p4server=10.23.0.1 --build-arg p4root=/home/freddy/source --build-arg p4user=freddy --build-arg p4port=34734 --build-arg release=`lsb_release -c | sed s/Codename://g | sed -e s/[[:space:]]//g` -f Dockerfile 

