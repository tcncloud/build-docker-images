FROM golang:1.11

RUN apt update && apt install -y unzip 

ENV PROTO_VERSION 3.6.1
RUN wget https://github.com/protocolbuffers/protobuf/releases/download/v${PROTO_VERSION}/protoc-${PROTO_VERSION}-linux-x86_64.zip && \
  unzip protoc-${PROTO_VERSION}-linux-x86_64.zip -d /usr/local && \
  rm protoc-*

RUN go get -u github.com/golang/protobuf/protoc-gen-go@v1.2.0
