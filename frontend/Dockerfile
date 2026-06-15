
FROM node:20-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
ENV PATH=/app/node_modules/.bin:$PATH
COPY . .
RUN npx next build
EXPOSE 3000
CMD ["npm","start"]
