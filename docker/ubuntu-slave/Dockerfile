FROM ubuntu:19.04

#update image
RUN apt-get update

#install dependencies for docker
RUN apt-get install -y \
        apt-transport-https \
        ca-certificates \
        curl \
        gnupg-agent \
        software-properties-common
# add docker key
RUN curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add -

RUN add-apt-repository \
       "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
       $(lsb_release -cs) \
       stable"

RUN apt-get update

RUN apt-get install -y docker-ce docker-ce-cli containerd.io

#ENTRYPOINT ["/bin/bash"]
#CMD ["pwd"]
#CMD ["docker", "--version"]
#CMD ["bash"]

#CMD ["nginx", "-g", "daemon off;"]
