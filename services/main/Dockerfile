FROM node:latest

# set working directory
RUN mkdir /main
WORKDIR /main

# add `/usr/src/main/node_modules/.bin` to $PATH
ENV PATH /usr/src/main/node_modules/.bin:$PATH

# install and cache app dependencies
# ADD package.json /usr/src/main/package.json
COPY package.json ./
COPY package-lock.json ./
RUN npm install --silent

# add main
COPY . ./

# start main
CMD ["npm", "start"]