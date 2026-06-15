
FROM node:20-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
RUN npm install -g next
RUN next build
EXPOSE 3000
CMD ["npm","start"]
