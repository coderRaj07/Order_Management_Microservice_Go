export PATH="$PATH:$(sudo go env GOPATH)/bin"

sudo go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.28

sudo go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.2

sudo apt-get install protobuf-compiler

protoc-gen-go-grpc --version

make gen