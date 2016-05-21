FROM ubuntu:xenial
MAINTAINER Karthik Nishanth

RUN perl -pi -e 's/#force_color_prompt=yes/force_color_prompt=yes/g' /root/.bashrc

RUN perl -pi -e 's/archive.ubuntu.com/ftp.iitm.ac.in/g' /etc/apt/sources.list
RUN apt-get update

RUN apt-get install build-essential git python python3-pip

ENTRYPOINT /bin/bash
WORKDIR /root