# Dockerfile
FROM node:14

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Replace git protocol with https
RUN git config --global url."https://".insteadOf git://

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose the port the app runs on
EXPOSE 80

# Start the app
CMD ["npm", "start"]
