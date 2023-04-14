FROM mongo:latest

RUN apt-get update && apt-get install -y gnupg wget && \
    wget -qO - https://www.mongodb.org/static/pgp/server-5.0.asc | apt-key add - && \
    echo "deb http://repo.mongodb.org/apt/debian buster/mongodb-org/5.0 main" | tee /etc/apt/sources.list.d/mongodb-org-5.0.list && \
    apt-get update && apt-get install -y mongo-tools && \
    rm -rf /var/lib/apt/lists/*

CMD ["mongod"]






