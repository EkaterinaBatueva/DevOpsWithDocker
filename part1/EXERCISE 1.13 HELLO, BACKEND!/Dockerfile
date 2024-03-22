FROM ubuntu:latest

COPY . .

EXPOSE 8080

RUN apt-get update && apt-get install -y wget gcc && rm -rf /usr/local/go && wget https://go.dev/dl/go1.16.15.linux-amd64.tar.gz && tar -C /usr/local -xzf go1.16.15.linux-amd64.tar.gz

ENV PATH /usr/local/go/bin:$PATH

RUN go build

RUN go test

CMD ["./server"]
