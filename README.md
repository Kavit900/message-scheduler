# message-scheduler


# Installation Steps on MAC :-

-> Install golang version greater or equal to 1.6

-> Run the following belows command in your terminal
	go get -u google.golang.org/grpc
	go get -u github.com/micro/protobuf/{proto,protoc-gen-go}
	go get -u github.com/golang/protobuf/protoc-gen-go
	go get -u github.com/grpc-ecosystem/grpc-gateway/protoc-gen-grpc-gateway
	go get golang.org/x/sys/unix
	brew install protobuf
	export GOPATH=$HOME/go
	export PATH=$PATH:$GOPATH/bin

-> Whenever you run Makefile and pb.go file gets created, don't forget to perform - go get -u -f github.com/Kavit900/message-scheduler/consignment-service
This will bring your code relatvie to $GOPATH/src folder and you will be able to import it inside your main.go file

# Benefits of Dockerizing your application

-> Containers don't contain a kernel, a guest OS or any lower level components 
-> Containers only contain the top level libraries and it's run time components. 
-> The Kernel is shared across the host machine. So host machine runs a single Unix kernel, then it is shared by n amounts of containers, running very different sets of run-times.
-> Containers utilise kernel utilities, in order to share resources and network functionality across the container space.

# How we can tackle hard coded location of the service address

-> Problem arises when our services are running in the cloud, they may not share the same host or the address or ip may change after re-deploying a service.
-> We can tackle this with service discovery. Service discovery keeps an up-to-date cataloque of all your services and their locations. 
-> Each Service registers itself at runtime and de-registers itself on closure. Name or id assigned to it.

# Go-micro

-> Powerful microservice framework written in Go.
