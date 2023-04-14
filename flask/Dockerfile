FROM python:latest


WORKDIR  /usr/src/app/

COPY app.py /usr/src/app/
COPY connect_to_mongoDB.py /usr/src/app/
COPY connect_to_TMDB.py /usr/src/app/
COPY passwords_and_keys.py /usr/src/app/
COPY templates /usr/src/app/
COPY static /usr/src/app/


RUN pip install flask pymongo requests Pillow

EXPOSE 5000

CMD ["python", "/usr/src/app/app.py"]
