# Use an official Node runtime as the base image
FROM node:20-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json from the local project into /app
COPY ../my-world-fe/package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application files from the local project
COPY ../my-world-fe/ ./

# Build the Next.js application
RUN npm run build

# Expose the port the app runs on
EXPOSE 3000

# Define the command to run the app
CMD ["npm", "run", "dev"]
