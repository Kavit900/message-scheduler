# message-scheduler


# Installation Steps on MAC :-

-> Install golang version greater or equal to 1.6

-> Run the following belows command in your terminal
	go get -u google.golang.org/grpc
	go get -u github.com/golang/protobuf/protoc-gen-go
	go get -u github.com/grpc-ecosystem/grpc-gateway/protoc-gen-grpc-gateway
	brew install protobuf
	export GOPATH=$HOME/go
	export PATH=$PATH:$GOPATH/bin

-> Whenever you run Makefile and pb.go file gets created, don't forget to perform - go get -u -f github.com/Kavit900/message-scheduler/consignment-service
This will bring your code relatvie to $GOPATH/src folder and you will be able to import it inside your main.go file