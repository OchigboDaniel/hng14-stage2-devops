FROM python:3.11-slim

# Create non-root user
RUN useradd -m appuser

WORKDIR /app

# Install dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy app
COPY . .

# Switch to non-root
USER appuser

# Healthcheck
HEALTHCHECK CMD curl --fail http://localhost:8000 || exit 1

# Run app
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
