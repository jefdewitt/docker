# Use an official Python runtime as a parent image
FROM nginx

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
ADD . /app

# Install any needed packages specified in requirements.txt
# RUN apt-get -qq update && apt-get -qq -y install curl && curl -sL https://deb.nodesource.com/setup_6.x | bash && apt-get -qq -y install nodejs && npm install jquery@3.2.1

# Make port 80 available to the world outside this container
EXPOSE 80

# Define environment variable
ENV NAME World

# Run scripts.js when the container launches
# CMD ["jquery", "scripts.js"]
CMD echo 'Herro Jefe'