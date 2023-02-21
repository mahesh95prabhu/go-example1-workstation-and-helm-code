FROM golang:1.20-alpine

WORKDIR /app

COPY go.mod ./
#COPY go.sum ./
RUN go mod download

COPY *.go ./

RUN mkdir static
RUN go build -o /go-example1-docker

EXPOSE 5000

CMD [ "/go-example1-docker" ]