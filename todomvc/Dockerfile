# Dockerfile
FROM node:14

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Set npm registry to use HTTPS
RUN npm config set registry https://registry.npmjs.org/

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose the port the app runs on
EXPOSE 80

# Start the app
CMD ["npm", "start"]
