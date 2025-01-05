# Use Node.js version 20.14 as the base image
FROM node:20.14

# Set the working directory inside the container
WORKDIR /app

# Copy only package.json and package-lock.json to install dependencies first
COPY package*.json ./

# Install backend dependencies
RUN npm install

# Copy the rest of the backend application files into the container
COPY . .

# Expose the port the backend runs on
EXPOSE 3001

# Start the backend application
CMD ["node", "server.js"]
