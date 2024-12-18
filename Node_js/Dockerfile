#Base image
FROM node:16-alpine

#set eniroment variable
ENV NODE_ENV=production
ENV PORT=3000

#Create app directory
WORKDIR /app

#copy package file and install dpendencies
COPY package*.json ./
RUN npm install

#copy the rest of the application code
COPY . .

#Expose the application port
EXPOSE $PORT

#Run the application
CMD ["npm", "start"]