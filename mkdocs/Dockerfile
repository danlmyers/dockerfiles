FROM python:3.4

COPY ./requirements.txt /

EXPOSE 8000
RUN pip install -r /requirements.txt

RUN mkdir /documents
RUN mkdir /site
WORKDIR /documents

CMD mkdocs serve
