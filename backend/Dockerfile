# Use the official Node.js image as the base image
FROM node:14

# Set the working directory inside the container
WORKDIR /backend

# Copy the package.json and package-lock.json files to the working directory
COPY package*.json ./

# Install the dependencies
RUN npm install

# Copy the rest of the application code to the working directory
COPY . .

# Expose the port the app runs on
EXPOSE 4000

# Define the command to run the application
CMD ["npm", "start"]  # Or CMD ["node", "server.js"]