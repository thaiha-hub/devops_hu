# As required, the image is based on node 16.x 
FROM node:16
# Set working directory
WORKDIR /app

RUN node -v & npm -v

# Copy package.json and package-lock.json, these files that tell Node what dependencies to install by using command >> npm install<<
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the project into the WORKDIR
COPY . .

# Expose the port that the app listens on
EXPOSE 3000

# Command to start the app
CMD ["npm", "start"]

