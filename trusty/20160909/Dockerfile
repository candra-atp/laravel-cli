FROM dockerkit/ubuntu:trusty-20160909

RUN export DEBIAN_FRONTEND=noninteractive \
    && apt-get update \
    && apt-get install --no-install-recommends -yq \
       curl \
       ca-certificates \
    && apt-get install --no-install-recommends -yq \
       vim \
       git \
       php5-cli \
       php5-curl \
       php5-intl \
       php5-json \
       php5-mcrypt \
       php5-mysqlnd \
       php5-pgsql \
       php5-readline \
       php5-sqlite \
       php5-xsl \
    && php5enmod \
       curl \
       intl \
       json \
       mcrypt \
       mysqlnd \
       pgsql \
       readline \
       sqlite \
       xsl \ 
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN export DEBIAN_FRONTEND=noninteractive \
    && apt-get update \
    && curl -sL https://deb.nodesource.com/setup_6.x | bash - \
    && apt-get install --no-install-recommends -yq \
       nodejs \
       g++ \
       python \
       make \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN npm install --global npm \
    && npm install --global gulp \
    && npm cache clean

RUN curl -sL https://getcomposer.org/download/1.2.0/composer.phar -o /usr/local/bin/composer.phar \
    && chmod a+x /usr/local/bin/composer.phar \
    && ln -s /usr/local/bin/composer.phar /usr/local/bin/composer

