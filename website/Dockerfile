FROM library/node:14.5.0-alpine

ARG NODE_ENV

WORKDIR /web

COPY ./src/package.json ./
COPY ./src/yarn.lock ./
RUN yarn install

COPY ./src .
RUN yarn run build