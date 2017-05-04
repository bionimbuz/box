FROM ubuntu:trusty
MAINTAINER Tiago Alves "tiagoalves83@gmail.com"

ENV CUFFLINKS_LINK http://cole-trapnell-lab.github.io/cufflinks/assets/downloads/cufflinks-1.2.1.Linux_x86_64.tar.gz

ENV PATH /bin/cufflinks:$PATH

RUN apt-get -y update && apt-get -y install \
  wget 

RUN sudo wget -O cufflinks.tar.gz $CUFFLINKS_LINK

RUN sudo tar xzvf cufflinks.tar.gz -C /bin && mv /bin/cufflinks* /bin/cufflinks

ENTRYPOINT ["/bin/cufflinks/cufflinks"]
CMD ["--help"]
