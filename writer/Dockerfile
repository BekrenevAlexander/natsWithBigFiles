FROM node:15.7.0-alpine3.10
WORKDIR /usr/app/reader
COPY package.json .
RUN npm install --quiet
COPY . .
RUN npm i -g npx --force
RUN npx tsc
RUN npm i -g pm2 --force
RUN pm2 start ./build/index.js
