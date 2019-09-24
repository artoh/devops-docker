FROM ubuntu:16.04

WORKDIR /files

RUN apt-get update && apt-get install python3 ffmpeg

RUN pip3 install --user --upgrade yle-dl

ENTRYPOINT ["yle-dl"] 
