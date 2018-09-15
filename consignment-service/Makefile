build:
	export PATH=$PATH:$GOPATH/bin
	protoc -I/usr/local/include -I. -I$(GOPATH)/src -I$(GOPATH)/src/github.com/grpc-ecosystem/grpc-gateway/third_party/googleapis --go_out=plugins=micro:. proto/consignment/consignment.proto
	go get -u -f github.com/Kavit900/message-scheduler/consignment-service
	GOOS=linux GOARCH=amd64 go build
	docker build -t consignment-service .

run:
    docker run -p 50051:50051 \
        -e MICRO_SERVER_ADDRESS=:50051 \
        -e MICRO_REGISTRY=mdns consignment-service

 # -e is an environment variable flag, this allows you to pass in environment variables into your Docker container. 