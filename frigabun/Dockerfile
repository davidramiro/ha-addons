ARG BUILD_FROM
FROM $BUILD_FROM

ENV LANG C.UTF-8

RUN apk add --no-cache git make musl-dev go

# Configure Go
ENV GOROOT /usr/lib/go
ENV GOPATH /go
ENV PATH /go/bin:$PATH

RUN mkdir -p ${GOPATH}/src ${GOPATH}/bin

WORKDIR $GOPATH/src
RUN git clone https://github.com/davidramiro/frigabun.git

WORKDIR $GOPATH/src/frigabun
RUN go mod download

RUN CGO_ENABLED=0 GOOS=linux go build -o /frigabun
EXPOSE 9595

CMD ["/frigabun"]