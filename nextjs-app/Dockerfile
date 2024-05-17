# Use a base image with Node.js installed
FROM node:14-alpine

# Set working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json files
COPY package*.json ./

# Increase memory allocation for Node.js during npm install
ENV NODE_OPTIONS="--max-old-space-size=2048"

# Install dependencies
RUN npm config set strict-ssl false && npm install

# Copy the rest of the application files to the container
COPY . .

# Your remaining Dockerfile commands...
EXPOSE 3000

# Command to start the Next.js app
CMD ["npm", "run", "dev"]
