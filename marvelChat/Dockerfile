From ubuntu:16.04

# Install necessary packages
RUN apt update
RUN apt install cmake gcc make libc-dev g++ bzip2 libssl-dev build-essential wget -y
RUN apt install python3 python3-pip -y


# Hop into /marvelChat
WORKDIR /marvelChat

# Install Python requirements
COPY ./marvelChat/requirements.txt ./requirements.txt
RUN export C_INCLUDE_PATH=/usr/include
RUN pip3 install --upgrade pip
RUN pip3 install -r ./requirements.txt

# Hop into /
WORKDIR /marvelChat/src
CMD python3 ./server.py


