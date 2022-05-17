# Build arg variable 'p4clientspec' to store the name of the perforce clientspec   
ARG p4clientspec = ''
# Build arg variable 'p4server' to store the name of the perforce server   
ARG p4server = ''
# Build arg variable 'p4port' to store the name of the perforce port   
ARG p4port = ''
# Build arg variable 'p4ticket' to store the location of '.p4tickets' file    
ARG p4tickets = ''
# Build arg variable 'p4root' to store the location of local P4 workspace    
ARG p4root = ''

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
ADD $p4tickets /home/$username/.p4tickets

# Set Environment variable P4USER to the username 
ENV P4USER=$username 
# Set Environment variable P4ROOT  
ENV P4ROOT=$p4root
# Set Environment variable P4CLIENT  
ENV P4CLIENT=new_clientspec
# Set Environment variable P4PORT  
ENV P4PORT=$p4server:$p4port

RUN p4 client -t $p4clientspec new_clientspec
