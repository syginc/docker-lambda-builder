FROM amazonlinux:2023.7.20250428.1

RUN dnf -y groupinstall 'Development Tools' && \
  dnf -y install python3-pip nasm cmake && \
  # pip-2.7 install pipenv && \
  pip-3.9 install pipenv && \
  curl -fsSL https://rpm.nodesource.com/setup_20.x -o nodesource_setup.sh && \
  bash nodesource_setup.sh && \
  curl --silent --location https://dl.yarnpkg.com/rpm/yarn.repo | tee /etc/yum.repos.d/yarn.repo && \
  dnf -y install yarn && \
  dnf -y clean all

# For pipenv
ENV LANG en_US.UTF-8
