FROM ubuntu:20.04

# I am setting the workdir
WORKDIR /usr/src/app

# I am copying the local loop.sh script in the current workdir
COPY loop.sh .

# Get updates
RUN apt-get update

# Install curl
RUN apt-get -y install curl

# Add permissions
RUN chmod +x loop.sh

# Start the script
CMD ./loop.sh
