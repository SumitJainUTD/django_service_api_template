FROM python:3.8.10
# USER app
ENV PYTHONUNBUFFERED 1
# RUN mkdir /db
#RUN chown app:app -R /db

RUN mkdir /service_api
WORKDIR /service_api
ADD ./requirements.txt /service_api
RUN pip install -r requirements.txt
ADD . /service_api

EXPOSE 8000
RUN echo ls
CMD [ "python", "./manage.py", "runserver", "0.0.0.0:8000" ]