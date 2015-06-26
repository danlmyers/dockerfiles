FROM python:3.4

COPY ./requirements.txt /

EXPOSE 9010
RUN pip install -r /requirements.txt

run mkdir /documents
WORKDIR /documents

CMD mkdocs serve
