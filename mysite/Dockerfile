# Use an official Python runtime as a parent image
FROM python:3.7

# Set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install dependencies
RUN pip install --upgrade pip
RUN pip install -r requirements.txt

# Expose the port on which your Django app will run
EXPOSE 8000

# Run the Django app
CMD [ "python", "manage.py", "runserver", "0.0.0.0:8000" ]