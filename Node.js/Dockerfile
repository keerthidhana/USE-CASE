FROM node:20-alpine
WORKDIR /app
COPY node-service/package*.json ./
RUN npm ci
COPY node-service .
CMD ["node","index.js"]
 
