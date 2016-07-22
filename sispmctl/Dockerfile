FROM armbuild/debian:latest
 
MAINTAINER Kevin Taron <kevin.taron@gmail.com>
 
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install libusb-dev -y
RUN apt-get install build-essential -y
RUN apt-get install -y pkg-config
RUN wget http://downloads.sourceforge.net/project/sispmctl/sispmctl/sispmctl-4.0/sispmctl-4.0.tar.gz
RUN tar xzvf sispm*.tar.gz
WORKDIR "/sispmctl-4.0"
RUN ./configure
RUN make
RUN make install
RUN ldconfig
