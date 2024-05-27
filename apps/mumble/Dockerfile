# https://github.com/mumble-voip/mumble
FROM alpine

RUN apk update && apk add murmur

EXPOSE 64738

CMD ["murmurd", "-fg", "-v"]
