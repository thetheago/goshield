FROM golang:1.26.2-alpine AS builder

WORKDIR /app
COPY go.mod .
RUN go mod download

COPY . .
RUN go build -o goshield ./cmd/server

FROM alpine:3.22

WORKDIR /app
COPY --from=builder /app/goshield .

EXPOSE 8080
CMD ["./goshield"]
