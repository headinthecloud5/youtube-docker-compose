# Use the official Python image as the base image
FROM python:3.9-slim

# Set environment variables for Flask
ENV FLASK_APP=app.py \
	FLASK_RUN_HOST=0.0.0.0 \
	FLASK_RUN_PORT=8000

# Set the working directory in the container
WORKDIR /app

# Copy the requirements.txt file and install dependencies
COPY requirements.txt requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copy the entire application directory into the container
COPY . .

# Expose the port on which the Flask app will run
EXPOSE 8000

# Command to run the Flask application
CMD ["flask", "run", "--port", "8000"]

