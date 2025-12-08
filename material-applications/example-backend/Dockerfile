# golang 
FROM golang:1.16

# Working directory
WORKDIR /app

# Copy dependencies files
COPY go.* ./

# Download dependencies
RUN go mod download

# Copy the source code
COPY . .

# Expose the application port
EXPOSE 8080

RUN go build -o server .

CMD ["./server"]
