FROM python:3-onbuild
MAINTAINER Erik Rivas "jerivas@uaq.edu.mx"

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update \
		&& apt-get install -y octave less python-scipy libblas-dev liblapack-dev gfortran redis-server \
		&& apt-get autoclean && apt-get clean \
		&& rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* 


RUN pip install flask numpy oct2py scipy 
RUN pip install redis rq rq-dashboard
RUN pip install mysql-connector-python --allow-external mysql-connector-python 


VOLUME ["/src"]
WORKDIR /src

#CMD ["octave"]
#CMD ["python3"]

CMD ["/bin/bash"]

