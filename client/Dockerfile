
FROM node:lts-alpine

EXPOSE 8080

RUN mkdir /app

WORKDIR /app

# ENV PATH /app/node_modules/.bin:$PATH

COPY yarn.lock /app

COPY . /app

RUN chmod +x ./entrypoint.sh 