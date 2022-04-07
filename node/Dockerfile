
FROM node:argon

MAINTAINER User

RUN npm install -g nodemon

ADD package.json /tmp/package.json

RUN cd /tmp && npm install

RUN mkdir -p /src && cp -a /tmp/node_modules /src/

RUN npm install mysql

WORKDIR /src
ADD . /src

EXPOSE  8080

CMD ["nodemon", "/src/index.js"]
