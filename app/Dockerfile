# FROM golang
# WORKDIR /app
# EXPOSE 4000
# COPY go.mod ./
# # COPY go.sum ./

# RUN go mod download
# COPY . ./
# RUN go build -o main ./cmd/web

# CMD [ "/app/main" ]

FROM golang:1.20rc1-alpine3.17
WORKDIR /usr/src/app
# pre-copy/cache go.mod for pre-downloading dependencies and only redownloading them in subsequent builds if they change
COPY go.mod go.sum ./
RUN go mod download && go mod verify

COPY . .
RUN go build -o main ./cmd/web

CMD ["/usr/src/app/main"]