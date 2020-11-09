FROM golang:1.13.4-alpine as builder
WORKDIR /
ADD echo-server/echo-server.go /echo-server.go
RUN go build -installsuffix "static" -ldflags "-s -w" echo-server.go

FROM alpine:3.7
COPY --from=builder /echo-server.go /echo-server.go
CMD ["/echo-server.go"]