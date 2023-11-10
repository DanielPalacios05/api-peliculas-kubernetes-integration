FROM python:3.11-slim-buster

RUN mkdir /api-peliculas

WORKDIR /api-peliculas

RUN apt-get update
RUN apt-get install -y curl

COPY . /api-peliculas/

RUN pip3 install -r /api-peliculas/requirements.txt

ENV FLASK_ENV "development"
ENV FLASK_APP "entrypoint:app"
ENV APP_SETTINGS_MODULE "config.default"
ENV PORT 5000

#init be and create schets}

EXPOSE ${PORT}


CMD [ "flask", "run" ,"-h" ,"0.0.0.0" ]
