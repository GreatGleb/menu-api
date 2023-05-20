FROM python:3.9-alpine

RUN mkdir code
WORKDIR code

ADD requirements.txt /code/
RUN pip install -r requirements.txt

ADD . /code/
ADD .env.docker /code/.env

ENV APP_NAME=MENU_API

CMD gunicorn menu_api.wsgi:application -b 0.0.0.0:8000
