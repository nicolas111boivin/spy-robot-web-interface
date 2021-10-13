FROM debian:latest

WORKDIR /
COPY * /
RUN apt-get update && apt-get install -y python3-opencv
RUN apt-get install python3 python3-pip python3-venv -y
RUN python3 -m venv venv && . venv/bin/activate && pip3 install pip --upgrade && pip3 install -r requirements.txt
EXPOSE 9999
CMD ["start.sh"]
ENTRYPOINT ["/bin/bash"]