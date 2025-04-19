FROM python:3.10-slim

# Set a working directory inside the container for the Flask app
WORKDIR /app

# Copy only the requirements file first to leverage Docker cache efficiently
COPY Flask/requirements.txt .

# Install Flask and any other dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the Flask application code into the container
COPY Flask/app.py .

# Expose the port Flask will run on
EXPOSE 5000

# Command to run the Flask app
CMD ["python", "app.py"]
