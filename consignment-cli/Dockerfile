# consignment-cli/Dockerfile

FROM golang:1.9.0 as builder

RUN go get -u -f github.com/Kavit900/message-scheduler/consignment-cli

# Set our workdir to our current service in the gopath
WORKDIR /go/src/github.com/Kavit900/message-scheduler/consignment-cli

# Copy the current code into our workdir
COPY . .

RUN go get -u github.com/golang/dep/cmd/dep

RUN dep init && dep ensure

RUN CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo .

FROM alpine:latest

RUN apk --no-cache add ca-certificates

RUN mkdir /app
WORKDIR /app

COPY --from=builder /go/src/github.com/Kavit900/message-scheduler/consignment-cli/consignment-cli .

CMD ["./consignment-cli"]