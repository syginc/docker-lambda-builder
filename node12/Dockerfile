FROM amazonlinux:2.0.20191217.0

RUN yum -y groupinstall 'Development Tools' && \
  yum -y install python2-pip python3 python3-pip nasm cmake && \
  pip-2.7 install pipenv && \
  pip-3.7 install pipenv && \
  curl --silent --location https://rpm.nodesource.com/setup_12.x | bash - && \
  curl --silent --location https://dl.yarnpkg.com/rpm/yarn.repo | tee /etc/yum.repos.d/yarn.repo && \
  yum -y install nodejs yarn && \
  yum -y clean all

# For pipenv
ENV LANG en_US.UTF-8
