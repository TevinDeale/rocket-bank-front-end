FROM node:current-alpine3.19

WORKDIR /app

COPY public/ public/
COPY jsconfig.json .
COPY package.json .
COPY pnpm-lock.yaml .
COPY vite.config.js .
COPY vue.config.js .
COPY proxyurl.env .env
COPY index.html .
COPY src/ src/

RUN apk update && npm install -g pnpm

RUN pnpm install
RUN pnpm build

EXPOSE 4173

ENTRYPOINT ["pnpm", "preview", "--host", "0.0.0.0"]