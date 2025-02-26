# Use a Node.js base image
FROM node:20-alpine

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package.json package-lock.json ./

# Install dependencies (including Angular CLI)
RUN npm install -g @angular/cli && npm install

# Copy the rest of the app files
COPY . .

# Expose the Angular development server port
EXPOSE 4200

# Start the Angular app
CMD ["ng", "serve", "--host", "0.0.0.0"]
