FROM ubuntu:latest

EXPOSE 5000

WORKDIR /usr/src/app

RUN apt-get update && apt-get -y install curl

RUN curl -sL https://deb.nodesource.com/setup_16.x | bash

RUN apt install nodejs

RUN npm install -g serve

COPY ["package-lock.json", "package.json", "./"]

RUN npm install

COPY . .

ENV REACT_APP_BACKEND_URL="http://localhost:8080"

RUN npm run build

CMD [ "serve", "-s", "-l", "5000", "build" ]