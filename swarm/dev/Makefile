.PHONY: build cluster test

default: build

build:
	go build -o bin/swarm    github.com/solidum-network/go-solidum/cmd/swarm
	go build -o bin/geth     github.com/solidum-network/go-solidum/cmd/geth
	go build -o bin/bootnode github.com/solidum-network/go-solidum/cmd/bootnode

cluster: build
	scripts/boot-cluster.sh

test:
	go test -v github.com/solidum-network/go-solidum/swarm/...
