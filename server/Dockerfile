# Use an official Node.js runtime as the base image
FROM node:20-slim

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install Node.js dependencies
RUN npm install

# Install build-essential for Linux-based containers
RUN apt-get update && apt-get install -y build-essential


# Copy all the source files to the working directory
COPY . .

# Expose port 8080 for serving the web application
EXPOSE 8080

# Command to start the Node.js HTTP server
CMD ["node", "server.js"]
