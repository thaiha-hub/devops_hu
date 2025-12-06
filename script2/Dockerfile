#Start from an image of Ubuntu
FROM ubuntu:24.04 

# working directory
WORKDIR /usr/src/app

COPY script2.sh .

RUN apt update && apt install -y curl

RUN chmod +x script2.sh

ENTRYPOINT ["./script2.sh"]

