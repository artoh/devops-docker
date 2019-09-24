FROM ubuntu:16.04

WORKDIR /files

RUN apt-get update && apt-get install -y python3 python3-pip ffmpeg wget && \ 
	pip3 install --upgrade yle-dl && \
	apt-get purge -y --auto-remove python3-pip && \
	rm -rf /var/lib/apt/lists*

ENTRYPOINT ["yle-dl"]
