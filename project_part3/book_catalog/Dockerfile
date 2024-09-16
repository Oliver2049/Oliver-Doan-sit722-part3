# Dockerfile for book_catalog microservice
FROM python:3.9.5-slim

# Set the working directory in the container
WORKDIR /app/

# Copy the current directory contents into the container at /app
COPY app /app/app

# Copy the requirements file into the container at /app
COPY requirements.txt /app/

# Install any dependencies
RUN pip install --no-cache-dir -r /app/requirements.txt 

# Run app.py when the container launches
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]