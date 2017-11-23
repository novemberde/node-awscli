
FROM ubuntu

RUN apt-get update -y && \
     apt-get upgrade -y && \
     apt-get install -y nodejs && \
     apt-get install -y build-essential git curl python-dev

# Install latest version of pip
RUN curl -O https://bootstrap.pypa.io/get-pip.py && python get-pip.py

# Install AWS CLI
RUN pip install awscli awsebcli

CMD ["/bin/bash"]