FROM ubuntu:16.04

RUN apt-get update

RUN apt-get install -y apt-utils

RUN apt-get install -y python3 python3-venv

RUN apt-get -y upgrade

RUN python3 -V

RUN python3 -m venv ospurge
#RUN source ospurge/bin/activate

RUN apt-get install -y python3-pip git
RUN python3 -m pip install git+https://git.openstack.org/openstack/ospurge

RUN ospurge -h

ENV OS_USERNAME=*************
ENV OS_PASSWORD=*************
ENV OS_TENANT_NAME=UKCloudTrainingLab1
ENV OS_AUTH_URL=https://cor00005.cni.ukcloud.com:13000/v2.0

RUN ospurge  --verbose --purge-own-project 

ENV OS_USERNAME=*************
ENV OS_PASSWORD=************
ENV OS_TENANT_NAME=UKCloudTrainingLab2
ENV OS_AUTH_URL=https://cor00005.cni.ukcloud.com:13000/v2.0

RUN ospurge  --verbose --purge-own-project 