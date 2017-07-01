FROM ubuntu:14.04
MAINTAINER riet
RUN mv /etc/apt/sources.list /etc/apt/sources.list.bak
ADD sources.list /etc/apt/sources.list
RUN cp /usr/share/zoneinfo/Asia/Shanghai  /etc/localtime
#RUN mkdir /root/.pip
#ADD pip.conf /root/.pip/pip.conf
RUN rm -f /bin/sh && \
    ln -s /bin/bash /bin/sh
RUN apt-get update && \
    apt-get install -y libmysqlclient-dev python-dev python-pip build-essential openssl libssl-dev \
                       libpcre3 libpcre3-dev zlib1g-dev gettext nfs-common unzip nginx \
                       libxml2-dev libxslt1-dev libffi-dev mysql-client
RUN pip install  --upgrade pip && \
    pip install Django==1.10.6 django-widget-tweaks MySQL-python xmltodict pytz libipa apk_parse_ph4 biplist \
                Flask Flask-Login Flask-SQLAlchemy Flask-RESTful Flask-HTTPAuth Flask-WTF \
                Flask-Script Flask-Admin Flask-Moment Flask-Migrate \
                flask-socketio flask_cors passlib enum34 gevent scrypt \
                requests tornado paramiko futures lettuce python-Levenshtein Appium-Python-Client Pillow \
                supervisor uwsgi \
                django-filter==1.0.2 djangorestframework==3.6.2 pycrypto
RUN pip uninstall -y selenium && pip install selenium=2.53
RUN apt-get clean
EXPOSE 80
EXPOSE 5000
EXPOSE 6000
EXPOSE 8000
EXPOSE 9001
CMD bash
