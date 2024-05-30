# Use the official Python image from the docker Hub
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

#Expose the port that the server will run on
EXPOSE 8000

# Run the server.py script
CMD [ "python", "server.py" ]