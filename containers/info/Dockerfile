# Use python:2-alpine
FROM python:3-alpine

# Copy in the requirements.txt file
COPY requirements.txt /requirements.txt

# Install the requirements
RUN pip install -r /requirements.txt

# Copy in the application
COPY app /app

# Setup Flask
ENV FLASK_APP=/app/infopage.py

ENTRYPOINT flask run -h '::' --no-reload --eager-loading --with-threads
