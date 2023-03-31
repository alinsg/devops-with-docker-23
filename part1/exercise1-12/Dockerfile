# I chose to install ubuntu because it already had bash
FROM ubuntu:latest

# I am notifying Docker that I will be exposing the port 5000
EXPOSE 5000

# I am setting the workdir
WORKDIR /usr/src/app

# I am updating packages and installing curl
RUN apt-get update && apt-get -y install curl

# I am getting node from the repository
RUN curl -sL https://deb.nodesource.com/setup_16.x | bash

# I am installing nodejs
RUN apt install nodejs

# I am installing serve globally
RUN npm install -g serve

# I am copying package.json and package-lock.json before in order to install the necessary packages and benefit from layer caching
COPY ["package-lock.json", "package.json", "./"]

# I am installing the packages
RUN npm install

# I am copying the source code
COPY . .

# I am building the assets
RUN npm run build

# I am serving build folder to the port 5000
CMD [ "serve", "-s", "-l", "5000", "build" ]