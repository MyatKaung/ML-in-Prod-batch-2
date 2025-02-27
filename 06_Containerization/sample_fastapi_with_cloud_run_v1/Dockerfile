# Use the official Python base image
FROM python:3.10.14

# Set the working directory
WORKDIR /app

# Copy only the requirements.txt first to leverage Docker cache
COPY requirements.txt .

# Upgrade pip
RUN pip install --upgrade pip

# Install application dependencies
RUN pip install -r requirements.txt

# Copy the rest of the application code
COPY . .

# Expose the application port
EXPOSE 8888

# Command to run the application
CMD ["python", "main.py"]
