FROM ubuntu:19.10
RUN apt-get update
RUN apt install -y \
  build-essential \
  lazarus-ide \
  zip \
&& rm -rf /var/lib/apt/lists/*
WORKDIR /source-code
CMD /bin/bash
