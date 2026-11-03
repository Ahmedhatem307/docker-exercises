FROM golang:1.16

WORKDIR /app

COPY go.mod go.sum ./

RUN go mod download

COPY . .

RUN go build

RUN go test ./...

EXPOSE 8080

ENV PORT=8080

ENV REQUEST_ORIGIN=https://example.com

CMD ["./server"]
