# Lock all the versions for a reproducible image
FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive
ENV LC_ALL=C.UTF-8
ENV LANG=C.UTF-8

RUN apt-get update

RUN apt-get install \
	apt-transport-https=2.0.4 \
	ca-certificates=20210119~20.04.1 \
	curl=7.68.0-1ubuntu2.4 \
	software-properties-common=0.98.9.4 \
	-y

# To ensure that the software we’re installing is authentic enter
RUN curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add


RUN add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
RUN add-apt-repository ppa:deadsnakes/ppa

RUN apt-get update

RUN apt-get install \
	docker-ce=5:19.03.13~3-0~ubuntu-focal \
	python3-pip=20.0.2-5ubuntu1.1 \
	-y

# Upgrade pip and setuptools to a more recent version
RUN pip3 install pip==20.2.3 setuptools==50.3.0

# Checking for a recent version of pip makes no
# sense if we have already locked the versions
RUN pip install \
	aws-sam-cli==1.20.0 \
	awscli==1.19.23 \
    six==1.15.0 \
	--disable-pip-version-check
