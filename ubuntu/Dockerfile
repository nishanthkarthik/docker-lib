FROM ubuntu:xenial
MAINTAINER Karthik Nishanth

RUN perl -pi -e 's/#force_color_prompt=yes/force_color_prompt=yes/g' /root/.bashrc

ENV DEBIAN_FRONTEND noninteractive

RUN perl -pi -e 's/archive.ubuntu.com/ftp.iitm.ac.in/g' /etc/apt/sources.list
RUN apt-get update
RUN apt-get upgrade -y


RUN apt-get install -y apt-utils
RUN apt-get install -y build-essential git python python3-pip

WORKDIR /root
ENTRYPOINT ["/bin/bash"]