FROM alpine:latest as git
WORKDIR /
RUN apk add git --no-cache
RUN git clone https://github.com/Darkrm/logindemo.client.git

FROM nginx:1.14.0-alpine
COPY logindemo.conf /etc/nginx/conf.d
COPY --from=git /logindemo.client /logindemo.client