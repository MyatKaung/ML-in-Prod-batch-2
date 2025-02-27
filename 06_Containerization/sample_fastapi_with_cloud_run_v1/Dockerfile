FROM python:3.10.14

WORKDIR /app

# Copy and install dependencies
COPY requirements.txt ./
RUN pip install --upgrade pip && pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code
COPY . .

# Set environment variable for Cloud Run
ENV PORT=8888

# Expose the port explicitly (hardcoded)
EXPOSE 8888

# Start the FastAPI app using the environment variable PORT
CMD ["python", "main.py"]
