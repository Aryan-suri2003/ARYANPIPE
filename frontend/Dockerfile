
FROM node:20-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
# removed global next install
COPY . .
ENV PATH=/app/node_modules/.bin:$PATH
RUN rm -rf .next && npm run build
EXPOSE 3000
CMD ["npm","start"]
