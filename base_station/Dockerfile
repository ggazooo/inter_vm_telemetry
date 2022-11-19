FROM alpine:3.17

RUN apk add npm

WORKDIR /base
COPY web_app/ .

# Install dependencies and build
RUN npm ci
RUN npm run build

ENV NODE_ENV production

CMD ["npx", "serve", "build", "-p", "80"]
