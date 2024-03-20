FROM alpine:3.19

WORKDIR /usr/src/app

COPY script.sh .

RUN apk update && apk add --no-cache curl

CMD ./script.sh
