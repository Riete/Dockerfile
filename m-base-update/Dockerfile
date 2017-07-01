FROM riet/m-base
RUN pip install django-filter==1.0.2 djangorestframework==3.6.2 pycrypto
RUN pip uninstall -y selenium && pip install selenium=2.53
RUN apt-get clean
CMD bash
