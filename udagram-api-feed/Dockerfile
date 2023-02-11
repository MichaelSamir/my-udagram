FROM node:14.18.0
# Create app directory
WORKDIR /usr/src/app
# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied where available (npm@5+)
COPY package*.json ./
RUN npm cache clean --force
RUN rm -rf node_modules
RUN npm i -f
# Bundle app source
COPY . .
EXPOSE 8080
CMD [ "npm", "run", "prod" ]