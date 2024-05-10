sudo go mod tidy

protoc-gen-go --version

sudo apt install protoc-gen-go


export PATH=$PATH:$(sudo go env GOPATH)/bin

sudo go get google.golang.org/grpc/cmd/protoc-gen-go-grpc

sudo go install google.golang.org/grpc/cmd/protoc-gen-go-grpc

protoc-gen-go-grpc --version