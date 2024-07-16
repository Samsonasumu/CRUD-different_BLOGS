# Use an official Python image as a base
FROM python:3.9-slim-buster

# Set the working directory
WORKDIR /app

# Copy the requirements file into the app directory
COPY requirements.txt ./

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code
COPY . .

# Set the environment variables (optional)
ENV PYTHONUNBUFFERED 1
ENV PYTHONDONTWRITEBYTECODE 1

# Expose the port your Django app will run on
EXPOSE 8000

# Command to run the Django app
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
