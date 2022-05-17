# Build arg variable 'codename' to store the Ubuntu codename
ARG codename=""
# Build arg variable 'username'to store the username
ARG username=''
# Build arg variable 'hostname' to store the host machine name to login using auto ssh 
ARG hostname=''


#Use the Ubuntu image with the particular code name
FROM ubuntu:$codename

#Add the user 
RUN useradd -m $username

# Add the .ssh directory from the host machine to docker build 
ADD /home/$username/.ssh /home/$username/.ssh
RUN echo "Host hostname\n\tStrictHostKeyChecking no\n" >> /home/$username/.ssh/config
