FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive


# アップデートや言語設定
RUN apt-get update
RUN apt-get -y install locales && \
    localedef -f UTF-8 -i ja_JP ja_JP.UTF-8
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL ja_JP.UTF-8
ENV TZ JST-9
ENV TERM xterm

# git関連とperlのインストール
RUN apt update && \
    apt install -y --no-install-recommends \
    build-essential \
    git \
    vim \
    curl \
    tree \
    ca-certificates \
    openssh-server \
    libyaml-tiny-perl \
    libfile-homedir-perl \
    libunicode-linebreak-perl && \
    apt -y clean && \
    rm -rf /var/lib/apt/lists/*


RUN mkdir -p /root/workspace
COPY texlive.profile /root/workspace
COPY .latexmkrc /root
WORKDIR /root/workspace

RUN curl -LO http://ftp.jaist.ac.jp/pub/CTAN/systems/texlive/tlnet/install-tl-unx.tar.gz
RUN mkdir install-tl && \
    tar xzf install-tl-unx.tar.gz -C install-tl --strip-components 1
# RUN ./install-tl/install-tl --profile texlive.profile
# RUN rm -r install-tl install-tl-unx.tar.gz

ENV PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ '
RUN echo "PS1='"${PS1}"'" >> ~/.bashrc

RUN echo 'PATH="$PATH:/usr/local/texlive/2023/bin/x86_64-linux"' >> ~/.bashrc
# RUN /usr/local/texlive/2023/bin/x86_64-linux/tlmgr path add
