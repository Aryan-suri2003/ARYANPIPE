FROM node:20-alpine

WORKDIR /app

COPY package*.json ./

RUN npm install

RUN echo "===== PACKAGE ====="
RUN cat package.json

RUN echo "===== NEXT ====="
RUN npm list next

RUN echo "===== BIN ====="
RUN ls -la node_modules/.bin

COPY . .

RUN echo "===== FILES ====="
RUN ls -la
RUN find . -maxdepth 2 -type f

RUN npm run build
