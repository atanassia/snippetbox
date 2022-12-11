FROM golang
WORKDIR /app
EXPOSE 4000
COPY go.mod ./
# COPY go.sum ./

RUN go mod download
COPY . ./
RUN go build -o /maindf ./cmd/web

CMD [ "/maindf" ]