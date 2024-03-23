FROM golang:1.19-alpine AS builder

WORKDIR /app

COPY go.mod go.sum ./

RUN go mod download

COPY . .

RUN go build -o server ./app.go 

FROM alpine:3.16

WORKDIR /app

COPY --from=builder /app/server .

EXPOSE 8080

CMD ["sh", "-c", "apk add curl && while true; do curl -f localhost:$PORT; sleep 10; done"]

ENTRYPOINT ["/app/server"]
