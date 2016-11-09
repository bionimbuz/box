FROM ubuntu:trusty
MAINTAINER Tiago Alves "tiagoalves83@gmail.com"

ENV TOPHAT_LINK https://ccb.jhu.edu/software/tophat/downloads/tophat-1.3.2.Linux_x86_64.tar.gz
ENV BOWTIE_LINK http://sourceforge.net/projects/bowtie-bio/files/bowtie/0.12.7/bowtie-0.12.7-linux-x86_64.zip
ENV SAMTOOLS_LINK http://sourceforge.net/projects/samtools/files/samtools/0.1.17/samtools-0.1.17.tar.bz2

ENV PATH /bin/tophat:/bin/bowtie/:/bin/samtools:$PATH

RUN apt-get -y update && apt-get -y install \
  gcc \
  bzip2 \
  python \
  unzip \
  wget \
  zlib zlib-devel

RUN wget -O tophat.tar.gz $TOPHAT_LINK
RUN wget -O bowtie.zip $BOWTIE_LINK
RUN wget -O samtools.tar.bz2 $_LINK

RUN tar xzvf tophat.tar.gz -C /bin && mv /bin/tophat* /bin/tophat
RUN unzip -o bowtie.zip -d /bin && mv /bin/bowtie* /bin/bowtie
RUN tar xjvf samtools.tar.bz2 -C /bin && /bin/samtools* /bin/samtools

RUN make -C /bin/samtools

ENTRYPOINT ["/bin/tophat"]
CMD ["--help"]
