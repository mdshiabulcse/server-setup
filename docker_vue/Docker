# Dockerfile

# Use Node.js version 22 Alpine (lightweight)
FROM node:22-alpine

# Set the working directory
WORKDIR /app

# Copy only package files first (for caching docker builds)
COPY package*.json ./

# Install dependencies
RUN npm install

# Now copy the entire project
COPY . .

# Expose the dev server port
EXPOSE 3000

# Start the Vite dev server
CMD ["npm", "run", "dev"]
