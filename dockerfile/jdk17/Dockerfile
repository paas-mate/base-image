FROM ttbb/base:latest

RUN dnf install -yq java-17-openjdk-devel && \
    dnf clean all
RUN wget https://github.com/alibaba/arthas/releases/download/arthas-all-3.6.3/arthas-bin.zip && \
    mkdir -p /opt/sh/arthas && \
    unzip arthas-bin.zip -d /opt/sh/arthas && \
    rm -rf arthas-bin.zip && \
    echo "alias arthas='java -jar /opt/sh/arthas/arthas-boot.jar'" >> /etc/bashrc

ENV JAVA_HOME /etc/alternatives/jre_17_openjdk
