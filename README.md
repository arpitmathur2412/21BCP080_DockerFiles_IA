# 21BCP080_DockerFiles_IA

**Steps to create dockerfile**

-Use an official Node.js runtime as the base image. If the image does not exists in the
 local docker repository, it will pull it from docker hub.

**FROM node:$VERSION**

- Set the working directory inside the container
**WORKDIR /app**

- Copy package.json and package-lock.json to the working directory

**COPY package*.json ./**

- Install the project dependencies from node package manager
If creating a nodejs server

**RUN npm install**

- Copy the rest of the backend code to the working directory

**COPY . .**

- Expose the port on which your backend server will run

**EXPOSE $PORT**

- Start the backend server 

**CMD ["npm", "start"]**
