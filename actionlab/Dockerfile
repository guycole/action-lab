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
RUN mkdir -p /opt/app/action-lab
COPY driver.py /opt/app/action-lab
COPY requirements.txt /opt/app/action-lab
WORKDIR /opt/app/action-lab
RUN pip install -r requirements.txt 

# start 
CMD ["python", "/opt/app/action-lab/driver.py"]
