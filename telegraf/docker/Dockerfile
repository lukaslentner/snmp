FROM telegraf:1.26.3

RUN apt-get update
RUN apt-get install -y software-properties-common
RUN apt-add-repository non-free
RUN apt-get update
RUN apt-get install -y snmp-mibs-downloader