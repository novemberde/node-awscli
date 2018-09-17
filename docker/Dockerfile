
FROM novemberde/node-awscli

# Install Docker
RUN apt-get update -y && \
    apt-get install -y \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common && \
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add - && \
    add-apt-repository \
    "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
    $(lsb_release -cs) \
    stable" && \
    apt-get update -y && \
    apt-get install docker-ce -y && \
    usermod -aG docker $(whoami)

CMD ["/bin/bash"]