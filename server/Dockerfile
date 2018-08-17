FROM alpine:latest as git
WORKDIR /
RUN apk add git --no-cache
RUN git clone https://github.com/Darkrm/logindemo.server.git

FROM node:8.11.4-alpine
COPY --from=git /logindemo.server /logindemo.server
WORKDIR ./logindemo.server
RUN npm install

EXPOSE 7777
CMD ["node", "app"]