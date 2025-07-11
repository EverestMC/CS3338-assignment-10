# Step 1: Use a Node.js base image. Choose the version that's appropriate for React.
# As with the backend, use a minimal version like alpine to reduce the image size.
FROM node:18-alpine 

# Step 2: Set the working directory inside the container.
# Use a folder name that matches the frontend code’s structure.
WORKDIR /app    

# Step 3: Copy package.json and package-lock.json (if present) first to install dependencies.
# You need this to install the React dependencies.
# Hint: you can copy both files with one command! Remember .gitignore formatting, it's very similar.
LABEL maintainer="mmcnall@calstatela.edu"
LABEL version="1.0"
LABEL description="Frontend for CS3338 Assignment 10"

# Step 4: Install the npm dependencies.
# Use a command that installs the dependencies from the package.json file.
COPY package*.json ./

# Step 5: Copy the rest of your frontend code into the container.
# This includes all source files, public assets, etc.
RUN npm install 

# Step 6: Expose the port for the React app to run on.
# React's development server typically runs on port 3000.
COPY . . 
# Step 7: Set the command to start your React app.
# This is usually the npm start command, but check your package.json.
EXPOSE 3000

CMD ["node", "server.js"] 
