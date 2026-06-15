FROM node:20-alpine

WORKDIR /app

COPY package*.json ./

RUN npm install

RUN npm list next
RUN ls -la node_modules/.bin

COPY . .

RUN npm run build
