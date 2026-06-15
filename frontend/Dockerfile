FROM node:20-alpine

WORKDIR /app

COPY package*.json ./

RUN npm install

RUN echo "ARYAN DEBUG"
RUN npm list next
RUN ls -la node_modules/.bin

COPY . .

RUN npm run build
