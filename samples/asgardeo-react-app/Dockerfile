# Use the official node:10-alpine image as the base image
FROM node:10-alpine

# Set the working directory to /app
WORKDIR /app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code to the container
COPY . .

# Set the environment variables
ENV HOST=0.0.0.0
ENV DISABLE_DEV_SERVER_HOST_CHECK=true
ENV DISABLE_DEV_SERVER_HTTPS=true

# Expose port 3000
EXPOSE 3000

# Start the application
CMD ["npm", "start"]
