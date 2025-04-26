# Use Python 3.10 with Alpine as the base image
FROM python:3.10-alpine AS builder

WORKDIR /app

# Install dependencies
RUN apk update && \
    apk add --no-cache git bash

# Copy requirements and install Python dependencies
COPY requirements.txt /app/
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application
COPY . /app/

# Set the entrypoint and default command
ENTRYPOINT ["python"]
CMD ["app.py"]
