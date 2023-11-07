# Use an official Node runtime as the base image
FROM node:14 as build

# Set the working directory
WORKDIR /usr/src/app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application source code
COPY . .

# Build the application
RUN npm run build --prod

# Use a lightweight HTTP server to serve the static files
FROM nginx:alpine
COPY --from=build /usr/src/app/dist/* /usr/share/nginx/html/

# Expose port 4200
EXPOSE 4200
