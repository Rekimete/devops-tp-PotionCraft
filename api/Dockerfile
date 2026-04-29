FROM python:3.11-slim

# Set working directory
WORKDIR /app

# Install dependencies
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

# Copy application code
COPY . .

# Expose port 80 (container)
EXPOSE 80

# Ensure logs are sent to stdout/stderr
ENV PYTHONUNBUFFERED=1

# Run the app with gunicorn for production
CMD ["gunicorn", "--bind", "0.0.0.0:80", "app:app", "--workers", "2"]

