FROM python:2.7

COPY . /opt/ashlar
WORKDIR /opt/ashlar

RUN apt-get update
RUN apt-get -y autoremove && apt-get install -y libgeos-dev binutils libproj-dev gdal-bin

pip install pip==9.0.1
pip install --process-dependency-links --allow-external -e git+https://github.com/azavea/ashlar.git@develop#egg=ashlar

CMD ['python', 'manage.py', 'runserver']
