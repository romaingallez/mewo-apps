# FROM ubuntu

# RUN apt-get update && apt-get install -y redis-server

# CMD ["redis-server"]

## DOING IT FROM SOURCE INSTEAD with a multi-stage 

FROM alpine as builder

RUN apk update && apk add build-base

WORKDIR /app

RUN wget http://download.redis.io/redis-stable.tar.gz -O redis-stable.tar.gz

RUN tar -xvzf redis-stable.tar.gz

WORKDIR /app/redis-stable

RUN make

RUN ls -la

FROM alpine

COPY --from=builder /app/redis-stable/src/redis-server /app/redis-server

CMD ["/app/redis-server"]
