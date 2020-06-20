FROM node:6.9.1
RUN apt-get update && apt-get -y install git
WORKDIR /opt

RUN git clone https://github.com/eriktews/arguesecure-online.git .

RUN npm install

ADD init.sh /init.sh

RUN chmod +x /init.sh

EXPOSE 3002 
ENTRYPOINT ["/init.sh"]
