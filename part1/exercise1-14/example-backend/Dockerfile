FROM ubuntu:latest

EXPOSE 8080

WORKDIR /usr/src/app

RUN apt-get update && apt-get -y install curl

RUN curl -L "https://golang.org/dl/go1.16.linux-amd64.tar.gz" | tar -C /usr/local -xzf -

ENV PATH="/usr/local/go/bin:${PATH}"

COPY . .

ENV REQUEST_ORIGIN="http://localhost:5000"

RUN ["go", "build"]

CMD ["./server"]