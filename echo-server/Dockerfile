FROM golang:1.14.11-alpine3.11
WORKDIR /go/src/app
ADD echo-server/echo-server.go .
RUN go build echo-server.go
CMD ["echo-server"]