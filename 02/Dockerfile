FROM golang:1.8-alpine
ADD . /go/src/hello-world
RUN go install hello-world

FROM alpine:latest
COPY --from=0 /go/bin/hello-world .
ENV PORT 8080
CMD ["./hello-world"]