ARG BUILD_FROM=hassioaddons/base:7.1.0
FROM $BUILD_FROM

ENV LANG C.UTF-8

RUN apk add --no-cache python3
RUN pip3 install paho-mqtt
RUN pip3 install apscheduler

COPY alpha2.py /
COPY run.sh /
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]
