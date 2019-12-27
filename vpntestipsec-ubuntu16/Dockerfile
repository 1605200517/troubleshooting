FROM ubuntu:16.04

RUN apt-get update &&\
    apt-get -y install nano strongswan-plugin-eap-mschapv2 libcharon-extra-plugins libstrongswan-extra-plugins strongswan-starter

COPY etc/ipsec.secrets /etc/ipsec.secrets
COPY etc/ipsec.conf /etc/ipsec.conf

RUN mkdir -p /etc/ipsec.d/ && ln -s /etc/ssl/certs /etc/ipsec.d/cacerts

