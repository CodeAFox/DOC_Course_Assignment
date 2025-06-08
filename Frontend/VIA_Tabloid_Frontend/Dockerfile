FROM node:22-alpine AS base

WORKDIR /app

#Copy packages to container
COPY package*.json ./
#Install the dependencies
RUN npm install

#Copy the source files
COPY . .

#Build the React app inside the container
RUN npm run build

FROM nginx:alpine

#Copy the files from the previous image built
COPY --from=base /app/dist /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]