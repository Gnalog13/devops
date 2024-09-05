FROM debian:stable-slim 

LABEL maintainer="17sda13@mail.ru"

RUN apt-get update && \
    apt-get install -y gcc g++ make cmake wget unzip && \
    rm -rf /var/lib/apt/lists/* 

WORKDIR /workspace

RUN wget https://www.sqlite.org/2018/sqlite-amalgamation-3260000.zip && \
    unzip sqlite-amalgamation-3260000.zip 

COPY CMakeLists.txt /workspace

CMD ["bash"]
