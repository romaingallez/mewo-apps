FROM alpine

RUN apk update && apk add postgresql

USER postgres

RUN initdb -D /var/lib/postgresql/data

EXPOSE 5432

CMD ["postgres", "-D", "/var/lib/postgresql/data"]
