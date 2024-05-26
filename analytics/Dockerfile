FROM --platform=linux/amd64 public.ecr.aws/docker/library/python:3.10-slim-buster as build

WORKDIR /app
# Copy the requirements file into the container at /app
COPY requirements.txt /app/

# Install any needed packages specified in requirements.txt
RUN python -m pip install --upgrade pip setuptools wheel
RUN python -m pip install -r requirements.txt

COPY . /app/

# Specify the command to run on container start
CMD ["python", "app.py"]