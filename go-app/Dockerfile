#build
FROM golang:1.21-alpine AS builder

WORKDIR /app

COPY main.go .

RUN go build main.go

#run
FROM alpine:3 AS runner


WORKDIR /app


COPY --from=builder /app/main /app

CMD ["./main"]