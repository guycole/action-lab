# 
# docker build . -t action-lab:1
# docker run --rm -it action-lab:1 /bin/sh
# docker run --rm action-lab:1
#
FROM python:3.9-buster

LABEL build_date="2022-12-21"
LABEL description="action-lab"
LABEL maintainer="guycole@gmail.com"

# application
RUN mkdir -p /opt/app
COPY driver.py /opt/app
COPY requirements.txt /opt/app
WORKDIR /opt/app
RUN pip install -r requirements.txt 

# start 
CMD ["python", "/opt/app/driver.py"]
