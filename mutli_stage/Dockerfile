#Stage 1: Build
FROM node:16 AS builder

WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run builder

#Stage 2: production 
FROM nginx:alpine

#copy build file to NGINX
COPY --from=builder /app/build /usr/share/nginx/html

#Expose port and start server
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]