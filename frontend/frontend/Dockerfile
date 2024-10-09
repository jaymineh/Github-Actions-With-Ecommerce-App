# Use an official Node.js runtime as a parent image
FROM node:14 as build

# env
ARG REACT_APP_API_URL
ENV REACT_APP_API_URL $REACT_APP_API_URL

# Set the working directory
WORKDIR /frontend

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Build the React application
RUN npm run build

# Expose port 3000 to the outside world
EXPOSE 3000

# Command to run the application
CMD ["npm", "start"]