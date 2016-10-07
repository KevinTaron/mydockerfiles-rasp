FROM openhab/openhab:armhf-offline
 
MAINTAINER Kevin Taron <kevin.taron@gmail.com>
 
RUN sudo apt-get update
RUN sudo apt-get upgrade -y
RUN sudo apt-get install libusb-dev -y
RUN sudo apt-get install build-essential -y
RUN sudo apt-get install -y pkg-config
RUN sudo wget http://downloads.sourceforge.net/project/sispmctl/sispmctl/sispmctl-4.0/sispmctl-4.0.tar.gz
RUN sudo tar xzvf sispm*.tar.gz
WORKDIR "sispmctl-4.0"
RUN sudo ./configure
RUN sudo make
RUN sudo make install
RUN sudo ldconfig
WORKDIR "/"
RUN sudo apt-get install python-dev python-openssl git -y
RUN sudo git clone https://github.com/adafruit/Adafruit_Python_DHT.git
WORKDIR "Adafruit_Python_DHT"
RUN sudo python setup.py install