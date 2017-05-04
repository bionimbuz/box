FROM ubuntu:trusty
MAINTAINER Tiago Alves "tiagoalves83@gmail.com"

RUN echo "deb http://cloud.r-project.org/bin/linux/ubuntu trusty/" >> /etc/apt/sources.list

RUN apt-get -y update && apt-get -y --force-yes install \
  r-base 

ENTRYPOINT ["R"]
