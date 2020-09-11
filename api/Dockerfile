FROM python:3.7-slim

WORKDIR /app

COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

COPY . .

ENV PYTHONUNBUFFERED=1

CMD gunicorn -c gunicorn_config.py flow_rolls.main:app
