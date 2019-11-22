FROM python:3.7.2-stretch
#RUN apk --update add bash nano
#ENV STATIC_URL /static
#ENV STATIC_PATH /var/www/app/static
ADD src/requirements.txt /var/www/requirements.txt
RUN pip install -r /var/www/requirements.txt
EXPOSE 8000
