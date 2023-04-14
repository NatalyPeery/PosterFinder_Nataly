FROM mongo:latest

COPY connect_to_mongoDB.py /usr/src/app/

EXPOSE 27017

CMD ["mongod", "--bind_ip_all"]
