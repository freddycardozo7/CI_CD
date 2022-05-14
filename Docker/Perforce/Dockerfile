FROM ubuntu:bionic

# Update Ubuntu packages
RUN apt-get update
RUN apt-get dist-upgrade -y

# Install wget and gnupg
RUN apt-get install -y wget gnupg

# Add perforce repo to apt

RUN wget -qO - https://package.perforce.com/perforce.pubkey | apt-key add -
RUN echo 'deb http://package.perforce.com/apt/ubuntu bionic release' > /etc/apt/sources.list.d/perforce.list
RUN apt-get update

# Actually install it

RUN apt-get install -y helix-p4d
