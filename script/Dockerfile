#Start from an image of Ubuntu
FROM ubuntu:24.04 
# working directory
WORKDIR /usr/src/app

COPY script.sh .

RUN apt update && apt install -y curl

RUN chmod +x script.sh

CMD ["./script.sh"]
