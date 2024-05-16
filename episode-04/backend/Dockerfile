FROM node:14-alpine
RUN apk update && \
    apk add --no-cache \
    python3 \
    build-base
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY ./src ./src
COPY .eslintrc.json ./
EXPOSE 3003
CMD ["node", "src/server.js"]