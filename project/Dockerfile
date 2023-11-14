FROM python
RUN mkdir /app
WORKDIR /app
COPY . /app
RUN apt-get update -y
#RUN apt-get install pkg-config -y
#RUN apt-get install -y python3-dev build-essential
#RUN apt-get install -y default-libmysqlclient-dev
#RUN pip3 install mysqlclient
RUN pip3 install -r requirements.txt
RUN pip3 install cryptography
EXPOSE 8080
ENTRYPOINT ["/bin/bash"]
CMD ["-c","python3 /app/manage.py migrate && python3 /app/manage.py runserver 0.0.0.0:8080"]
