FROM fedora:36

WORKDIR /opt/sh

RUN dnf install -yq iputils net-tools iproute telnet bind-utils && \
    dnf install -yq util-linux tree && \
    dnf install -yq tcpdump nc && \
    dnf install -yq glibc-langpack-en procps lsof unzip perf sysstat wget iotop dstat systemtap-sdt-devel && \
    dnf install -yq openssl && \
    dnf install -yq dumb-init && \
    dnf update -yq vim-minimal && \
    dnf install -yq vim && \
    dnf clean all
RUN echo "alias ll='ls -al'" >> /etc/bashrc && \
    echo "alias ..='cd ..'" >> /etc/bashrc && \
    echo "alias ...='cd ../..'" >> /etc/bashrc && \
    echo "alias tailf='tail -f'" >> /etc/bashrc && \
    echo "set nu" >> /etc/vimrc && \
    ln -s /usr/bin/python3 /usr/bin/python && \
    groupadd sh -g 1024 && \
    useradd -r -g sh sh -u 1024 -m -d /home/sh

