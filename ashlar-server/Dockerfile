FROM python:2.7

ENV bin /usr/local/bin/

COPY . /opt/ashlar-server
WORKDIR /opt/ashlar-server

RUN apt-get update
RUN apt-get -y autoremove && apt-get install -y libgeos-dev binutils libproj-dev gdal-bin

RUN $bin/pip install pip==9.0.1
RUN $bin/pip install --process-dependency-links -e git+https://github.com/jeancochrane/ashlar.git@update-dependencies#egg=ashlar

RUN $bin/python manage.py migrate
CMD $bin/python manage.py runserver
