# Use Node.js version 20.14 as the base image for building the frontend
FROM node:20.14 AS build

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to install dependencies first
COPY package*.json ./

# Install frontend dependencies
RUN npm install

# Copy the rest of the frontend application files into the container
COPY . .

# Build the frontend application for production
RUN npm run build

# Use a lightweight NGINX server to serve the static files
FROM nginx:alpine

# Copy the build output from the build stage into the NGINX container
COPY --from=build /app/build /usr/share/nginx/html

# Expose port 80 (default port for NGINX)
EXPOSE 80

# Start the NGINX server
CMD ["nginx", "-g", "daemon off;"]
