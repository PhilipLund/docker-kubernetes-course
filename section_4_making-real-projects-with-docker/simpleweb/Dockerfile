# existing image
FROM node:alpine

#This places the app files in the usr/app to prevent overwriting folders (this could also be the home directory)
WORKDIR /usr/app

#Copy the files in the current directory to the container (index.js and package.json)
# first ./ is from second ./ is to NPM only needs package.json
COPY ./package.json ./

#install NPM dependency
RUN npm install

#copy all other files to the container to utalize cas
COPY ./ ./

#Default command to execute
CMD [ "npm", "start" ]
