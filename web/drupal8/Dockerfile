FROM drupal:8
MAINTAINER mrcelli@icloud.com

RUN apt-get update && apt-get install -y \
    nodejs \
    zip unzip \
    git \
    wget
RUN wget https://www.npmjs.com/install.sh && sh ./install.sh
RUN composer self-update --2 && npm install --global gulp-cli -y




