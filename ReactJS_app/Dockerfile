# dev
FROM node:16.10.0-alpine AS dev
ENV NODE_PATH /opt/app/node_modules

WORKDIR /opt/app/

COPY /*.json ./
RUN npm install

COPY . ./

CMD [ "npm", "start" ]

# prod
FROM node:16.10.0-alpine AS prod
ENV NODE_PATH /opt/app/node_modules

WORKDIR /opt/app

COPY /*.json ./
RUN npm install

COPY . ./
RUN npm build

CMD [ "npm", "start" ]
