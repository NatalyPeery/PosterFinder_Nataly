FROM python:latest

# Install gnupg and wget
RUN apt-get update && \
    apt-get install -y gnupg wget && \
    rm -rf /var/lib/apt/lists/*

# Add MongoDB repository
RUN wget -qO - https://www.mongodb.org/static/pgp/server-5.0.asc | apt-key add - && \
    echo "deb http://repo.mongodb.org/apt/debian buster/mongodb-org/5.0 main" | tee /etc/apt/sources.list.d/mongodb-org-5.0.list

# Install mongo-tools
RUN apt-get update && \
    apt-get install -y mongo-tools && \
    rm -rf /var/lib/apt/lists/*

# Set working directory
WORKDIR /usr/src/app

# Copy Python dependencies file and install dependencies
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

# Copy the Python script
COPY connect_to_mongoDB.py ./

# Expose port
EXPOSE 27017

# Run Python script
CMD ["python", "./connect_to_mongoDB.py"]




