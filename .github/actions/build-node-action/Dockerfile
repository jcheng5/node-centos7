FROM centos:centos7
LABEL maintainer="joe@rstudio.com"

RUN yum -y install centos-release-scl
RUN yum -y install python3 python3-pip
RUN yum -y install devtoolset-8
RUN yum -y install git
RUN yum -y install xz

COPY make-node.sh /make-node.sh

ENTRYPOINT [ "/make-node.sh" ]
