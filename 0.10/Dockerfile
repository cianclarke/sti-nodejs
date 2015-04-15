FROM openshift/base-centos7

# This image provides a Node.JS environment you can use to run your Node.JS
# applications.

MAINTAINER Jakub Hadvig <jhadvig@redhat.com>

# Image metadata
ENV FOO                   testity
ENV PORT                  8001
ENV NODEJS_VERSION        0.10
ENV IMAGE_DESCRIPTION     Node.js 0.10
ENV IMAGE_TAGS            node,nodejs,nodejs010
ENV IMAGE_EXPOSE_SERVICES ${PORT}:http

RUN yum install -y \
    https://www.softwarecollections.org/en/scls/rhscl/v8314/epel-7-x86_64/download/rhscl-v8314-epel-7-x86_64.noarch.rpm \
    https://www.softwarecollections.org/en/scls/rhscl/nodejs010/epel-7-x86_64/download/rhscl-nodejs010-epel-7-x86_64.noarch.rpm && \
    yum install -y --setopt=tsflags=nodocs nodejs010 && \
    yum clean all -y

USER default

EXPOSE ${PORT}
