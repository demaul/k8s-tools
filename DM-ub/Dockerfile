FROM ubuntu:18.04

COPY ./apt-key.gpg /app/apt-key.gpg

COPY ./kubernetes.list /app/kubernetes.list

RUN apt update

RUN apt install -y apt-transport-https gnupg ca-certificates

RUN apt-key add /app/apt-key.gpg

RUN mv /app/kubernetes.list /etc/apt/sources.list.d/

RUN apt update

RUN apt install -y kubectl

RUN mkdir ~/.kube

