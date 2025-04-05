# Stage 1: Install dependencies
FROM python:3.11 AS builder

WORKDIR /app

COPY requirements.txt .
RUN pip install --upgrade pip
RUN pip install -r requirements.txt

# Stage 2: Copy only what's needed to run the app
FROM python:3.11-slim

WORKDIR /app

# Copy installed packages from builder
COPY --from=builder /usr/local /usr/local

# Copy your app code
COPY app.py .

# Expose the port Flask runs on
EXPOSE 5000

# Start the app
CMD ["python", "app.py"]

