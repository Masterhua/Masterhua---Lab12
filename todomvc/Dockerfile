# Dockerfile for todomvc
FROM node:14

# Create app directory
WORKDIR /usr/src/app

# Copy package.json
COPY package.json ./

# Install yarn globally
RUN npm install -g yarn

# Install app dependencies using yarn
RUN yarn install

# Bundle app source
COPY . .

# Expose the port the app runs on
EXPOSE 8081

# Start the app
CMD ["yarn", "start"]
