FROM golang:alpine as build
ADD . /src
ADD go.mod go.sum ./
RUN go mod download
RUN cd /src && go build -o meu_go

FROM alpine
WORKDIR /app
COPY --from=build /src/meu_go /app
ENTRYPOINT ["./meu_go"]