FROM golang:latest AS gofish
WORKDIR /
ADD echo-server/echo-server.go /echo-server.go
RUN go build -installsuffix "static" -ldflags "-s -w" echo-server.go

FROM alpine:latest
COPY --from=gofish /echo-server.go /echo-server.go
CMD ["/echo-server.go"]