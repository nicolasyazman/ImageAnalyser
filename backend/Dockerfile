FROM python:3.6.12-alpine

COPY requirements.txt /

RUN python -m pip install -r /requirements.txt

COPY . /app
WORKDIR /app

EXPOSE 8000

CMD ["gunicorn"  , "--bind", "0.0.0.0:8000", "wsgi:app"]