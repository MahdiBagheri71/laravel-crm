# Use an official Node.js runtime as the base image
FROM node:16

# Set the working directory in the container to /app
WORKDIR /app

# Copy the package.json and yarn.lock files to the container
COPY ./src/fronted /app

# Install the application's dependencies
RUN yarn install

# Build the application
RUN yarn build

# Specify the command to run when the container starts
CMD [ "sh", "-c", "if [ \"$APP_ENV\" = \"development\" ]; then yarn dev; else yarn start; fi" ]
