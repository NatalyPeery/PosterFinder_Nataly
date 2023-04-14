FROM amazonlinux:2
RUN yum update -y
RUN yum install -y gnupg2 curl
RUN curl -fsSL https://www.mongodb.org/static/pgp/server-5.0.asc | apt-key add -
RUN echo "deb http://repo.mongodb.org/apt/amazonlinux/2/mongodb-org/5.0 main" | tee /etc/apt/sources.list.d/mongodb-org-5.0.list
RUN yum update -y
RUN yum install -y mongodb-org
EXPOSE 27017
CMD ["mongod"]
