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

# Add ENV to the frontend
ENV REACT_APP_BACKEND_URL=http://localhost:8080

RUN npm run build

RUN npm install -g serve

# Expose the port that the frontend listens on
EXPOSE 3000

# Command to start the app
CMD ["serve", "-s", "build", "-l", "3000"]

