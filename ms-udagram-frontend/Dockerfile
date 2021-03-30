# Use NodeJS base image
FROM node:13

ARG MAX_OLD_SPACE_SIZE=4096
ENV NODE_OPTIONS=--max-old-space-size=${MAX_OLD_SPACE_SIZE}

COPY . /www/app

RUN npm install -g cordova ionic
RUN npm install -g bower
RUN npm install -g gulp

WORKDIR /www/app
RUN npm install
RUN ionic build

EXPOSE 8100

CMD bash -c "ionic serve 8100 --adress 0.0.0.0"