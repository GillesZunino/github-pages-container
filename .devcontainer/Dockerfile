# -----------------------------------------------------------------------------------
# Copyright 2024, Gilles Zunino
# -----------------------------------------------------------------------------------


# "#################################################"
# Dockerfile to build a GitHub Pages Jekyll site
#   Github Depdendencies => https://pages.github.com/versions/
# "#################################################"
FROM ubuntu:latest

# "#################################################"
# "Define environment variables"
ENV RUBY_VERSION 3.3.4



# "#################################################"
# "Get the latest APT packages"
RUN apt-get update
RUN apt-get -y upgrade

# "#################################################"
# "Install Ubuntu prerequisites for Ruby and GitHub Pages (Jekyll)"
RUN apt-get -y install git \
    curl \
    autoconf \
    bison \
    build-essential \
    libssl-dev \
    libyaml-dev \
    libreadline6-dev \
    zlib1g-dev \
    libncurses5-dev \
    libffi-dev \
    libgdbm6 \
    libgdbm-dev \
    libdb-dev \
    apt-utils
    
# "#################################################"
# "GitHub Pages/Jekyll is based on Ruby. Set the version and path"
ENV RBENV_ROOT /usr/local/src/rbenv
ENV PATH ${RBENV_ROOT}/bin:${RBENV_ROOT}/shims:$PATH

# "#################################################"
# "Install rbenv to manage Ruby versions"
RUN git clone https://github.com/rbenv/rbenv.git ${RBENV_ROOT} \
  && git clone https://github.com/rbenv/ruby-build.git \
    ${RBENV_ROOT}/plugins/ruby-build \
  && ${RBENV_ROOT}/plugins/ruby-build/install.sh \
  && echo 'eval "$(rbenv init -)"' >> /etc/profile.d/rbenv.sh

# "#################################################"
# "Install ruby and set the global version"
RUN rbenv install ${RUBY_VERSION} \
  && rbenv global ${RUBY_VERSION}