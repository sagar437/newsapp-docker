FROM python:3.7.2-stretch
#Set working directory as /opt/project
WORKDIR /opt/project

# Copy server.py and requirements.txt to the working directory
COPY src/* /opt/project/
COPY src/requirements.txt /opt/project/

#Upgrade pip and install flask and gunicorn
RUN pip3 install --upgrade pip
RUN pip install -r requirements.txt
