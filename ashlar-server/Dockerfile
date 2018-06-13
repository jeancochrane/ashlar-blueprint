FROM quay.io/azavea/django:1.8-python2.7-slim

RUN apt-get update
RUN apt-get -y autoremove && apt-get install -y \
	libgeos-dev \
	binutils \
	libproj-dev \
	gdal-bin \
	git

COPY requirements.txt /tmp/

RUN pip install --process-dependency-links -r /tmp/requirements.txt

COPY . /opt/ashlar-server
WORKDIR /opt/ashlar-server
