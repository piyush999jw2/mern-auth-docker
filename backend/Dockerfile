# Base Image
FROM node:20-alpine

# Create working directory
WORKDIR /app

# Copy dependency files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy backend source code
COPY . .

# Application listens on port 5000
EXPOSE 5000

# Start the backend
CMD ["node", "server.js"]
