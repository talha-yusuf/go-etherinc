.PHONY: build cluster test

default: build

build:
	go build -o bin/swarm    github.com/etherinc/go-etherinc/cmd/swarm
	go build -o bin/geth     github.com/etherinc/go-etherinc/cmd/geth
	go build -o bin/bootnode github.com/etherinc/go-etherinc/cmd/bootnode

cluster: build
	scripts/boot-cluster.sh

test:
	go test -v github.com/etherinc/go-etherinc/swarm/...
