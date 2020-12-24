FROM rust:1.42
ENV DEBIAN_FRONTEND=noninteractive

RUN wget https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
RUN dpkg -i packages-microsoft-prod.deb
RUN apt update && apt install -y gcc make binutils libc6-dev gdb apt-transport-https less
RUN curl -sL https://deb.nodesource.com/setup_15.x | bash -
RUN apt-get install -y nodejs
RUN apt-get update && apt-get install -y dotnet-sdk-5.0
RUN git clone https://github.com/masaxsuzu/dotfiles.git ~/dotfiles && bash ~/dotfiles/deploy.sh
