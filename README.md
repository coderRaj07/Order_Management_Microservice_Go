## Go gRPC Microservices Example 🚀

This is an example of building microservices using Go and gRPC for efficient and scalable inter-service communication. It demonstrates how to:

- Use protocol buffers to define service interfaces 🎨
- Generate Go code from proto files 🔧
- Implement gRPC servers and clients in Go 💻
- Expose both gRPC and HTTP transports 🌐
- Organize code using clean architecture principles 🏗️

### Architecture 🏢

The example implements a simple order management system with the following microservices:

- **Order Service**: Handles creating and listing orders 📝
- **Kitchen Service**: Receives orders from the Order Service via gRPC 🍳
- **Browser Client**: Sends orders to the Kitchen Service via HTTP 🌐

The services communicate using a shared proto package generated from the proto definitions. This ensures type-safe communication between services. 🔒

### Running the Example 🏃‍♂️

1. Install protobuf compiler and Go gRPC plugins: 🔧

```bash
export PATH="$PATH:$(sudo go env GOPATH)/bin"
sudo go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.28
sudo go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.2
sudo apt-get install protobuf-compiler
```

2. Verify the installation of `protoc-gen-go-grpc`: 🔍

```bash
protoc-gen-go-grpc --version
```

3. Generate proto code: 🎨

```bash
make gen
```

4. Start the Order Service: 🚀

```bash
go run order/main.go
```

5. Start the Kitchen Service: 🍳

```bash
go run kitchen/main.go
```

6. Send an order via HTTP: 📤

```bash
curl -X POST -d '{"customer_id": 123, "product_id": 456, "quantity": 10}' http://localhost:8080/orders
```

7. Check the Kitchen Service logs for the received order. 🔍

### Improvements 🛠️

- Add database storage for orders 💾
- Implement more advanced order management features 🚀
- Add authentication and authorization 🔒
- Improve error handling and logging 📈

### Resources 📚

- [Go gRPC Basics Tutorial](https://grpc.io/docs/languages/go/basics/)
- [Protocol Buffers Language Guide](https://developers.google.com/protocol-buffers/docs/proto3)
- [Clean Architecture in Go](https://medium.com/@hatajoe/clean-architecture-in-go-4030f11ec1b1)

Citations:
[1] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/4781680/ce41e6c5-e585-448d-b6b3-40796269f102/paste.txt
[2] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/4781680/dd7b724c-a896-4afc-bb4a-4ef066a75ab2/paste-2.txt
[3] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/4781680/b18336d4-cd79-4591-83c0-82e861b66c01/paste.txt