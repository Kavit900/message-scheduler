build:
	go get -u -f github.com/Kavit900/message-scheduler/consignment-cli
	GOOS=linux GOARCH=amd64 go build
	docker build -t consignment-cli .

run:
	docker run -e MICRO_REGISTRY=mdns consignment-cli