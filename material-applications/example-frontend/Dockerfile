# Beginning with the existing image node.js ver.16 
FROM node:16
# creating a folder /app and starting working in the folder
WORKDIR /app

RUN node -v && npm -v

# Copy package.json and package-lock.json, these files that tell Node what dependencies to install by using command >> npm install<<
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy everything in the local  project folder into the container (/app)
COPY . .

# set the environment variable
ENV REACT_APP_BACKEND_URL=http://localhost:8080

RUN npm run build

RUN npm install -g serve

# Expose the port that the frontend listens on
EXPOSE 3000

# Command to start the app
CMD ["serve", "-s", "build", "-l", "3000"]

