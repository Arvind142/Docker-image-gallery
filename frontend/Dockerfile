#base image
# we are using alpine as it is lightweight image
FROM node:15.14-alpine

#working directory
WORKDIR /app

#expose port
EXPOSE 3000

#copy required files
COPY package.json package-lock.json ./

#install dependencies
RUN npm install --silent

#copying all files
COPY . ./

#runnnig code
CMD ["npm", "start"]