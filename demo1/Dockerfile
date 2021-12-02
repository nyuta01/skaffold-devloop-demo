FROM golang:1.17 as dev

WORKDIR /app/

COPY go.mod go.sum ./
RUN go mod download

COPY . .
RUN CGO_ENABLED=0 GOOS=linux go build -o /main .

RUN go install github.com/cespare/reflex@latest
CMD reflex -r '(\.go$|go\.mod)' -s go run main.go

FROM alpine:3
WORKDIR /app/

COPY --from=dev /main .
CMD ["./main"]