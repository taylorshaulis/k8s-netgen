FROM golang:latest AS gofish
WORKDIR /
ADD echo-server/echo-server.go /echo-server.go
RUN GOOS=linux GOARCH=amd64 go build -ldflags="-w -s" echo-server.go
RUN chmod +x echo-server.go

FROM alpine:latest
COPY --from=gofish /echo-server.go /echo-server.go
CMD ["/echo-server.go"]