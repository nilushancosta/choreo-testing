# Use an official Python runtime as a parent image
FROM python:3.9-slim-buster

# Create a non-root user
RUN adduser --system myuser

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any necessary dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Make port 80 available to the world outside this container
EXPOSE 8080

# Define environment variable
ENV NAME World

# Switch to the non-root user
USER myuser

# Run app.py when the container launches
CMD ["python", "app.py"]
