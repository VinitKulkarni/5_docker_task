# Use the official Node.js image
FROM node:18

# Set the working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

ENV BACKEND_URI=http://backend:5000/submit

# Install dependencies
RUN npm install express body-parser axios
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose the app port
EXPOSE 3000

# Start the application
CMD ["node", "app.js"]
