FROM golang as build

WORKDIR /app
COPY main.go .

FROM golang:1.20rc1-alpine3.17 as main

WORKDIR /app
COPY --from=build /app .

CMD [ "go", "run", "main.go" ]