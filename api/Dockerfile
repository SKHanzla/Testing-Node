# Use an official Node.js runtime as the base image
FROM node:14

# Set the working directory in the container
RUN mkdir /user/src/app
WORKDIR /user/src/app

# Copy package.json and package-lock.json to the working directory
ENV PATH /user/src/app/node_modules/.bin:$PATH

COPY package*.json /user/src/app

# Install dependencies
RUN npm install

# Copy the rest of the application code to the working directory
COPY . .

# Expose the port the app runs on
EXPOSE 3000

# Command to run the application
CMD ["npm", "start"]