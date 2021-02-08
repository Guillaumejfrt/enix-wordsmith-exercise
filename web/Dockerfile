FROM golang:latest

COPY . /web-server

RUN go build /web-server/dispatcher.go

WORKDIR /web-server/static

CMD ./../../go/dispatcher
