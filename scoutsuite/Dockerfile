FROM python:3.10.0-slim-buster

ADD requirements.txt .

RUN pip install -U pip && \
    pip install pipenv awscli boto3 && \
    pip install -r requirements.txt
