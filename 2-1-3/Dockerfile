# From K Quickly Page 26, bsdtar does not install.
# Output states that bsdtar has been replaced with libarchive-tools

FROM python:3
RUN apt-get update
#RUN apt-get install -y bsdtar
RUN apt-get install -y libarchive-tools
RUN mkdir -p ~/.fonts; cd ~/.fonts
RUN curl "https://noto-website-2.storage.googleapis.com/pkgs/Noto-hinted.zip" | bsdtar -xvf-
RUN fc-cache -f -v
COPY . /app
WORKDIR /app
CMD python3 hello.py

