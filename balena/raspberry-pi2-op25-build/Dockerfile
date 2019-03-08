FROM vassoz/sdr-balena-raspberry-pi2-build

MAINTAINER Vasyl Petrushko <vassoz@gmail.com>

RUN [ "cross-build-start" ]

RUN echo 'blacklist dvb_usb_rtl28xxu' > /etc/modprobe.d/raspi-blacklist.conf

WORKDIR /

RUN git clone https://github.com/boatbod/op25.git && \
    cd op25 && \
    ./install.sh

RUN [ "cross-build-end" ]
