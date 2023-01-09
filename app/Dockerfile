FROM registry.redhat.io/ubi8/python-38:3.8
WORKDIR /app
COPY requirements.txt requirements.txt
COPY . .
RUN pip3 install -r requirements.txt
EXPOSE 5000
ARG USER_NAME demouser
ARG USER_PASS demopass
ENV USER_NAME $USER_NAME
ENV USER_PASS $USER_PASS
RUN echo $USER_NAME
RUN echo $USER_PASS
CMD ["python3", "-m","flask","run","--host=0.0.0.0"]

