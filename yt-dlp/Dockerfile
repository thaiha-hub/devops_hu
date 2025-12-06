FROM ubuntu:24.04

WORKDIR /mydir

#Update package lists and install curl, python3, and ffmpeg
RUN apt update && apt install -y curl
RUN apt install -y python3 ffmpeg

#Download yt-dlp and make it executable
RUN curl -L https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp -o /usr/local/bin/yt-dlp
RUN chmod a+rx /usr/local/bin/yt-dlp

#CMD ["/usr/local/bin/yt-dlp"]
#replace CMD with ENTRYPOINT to allow passing arguments when running the container
ENTRYPOINT ["/usr/local/bin/yt-dlp"]
