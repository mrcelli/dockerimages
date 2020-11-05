FROM drupal:8
MAINTAINER mrcelli@icloud.com

RUN apt-get update && apt-get install -y \
    nodejs \
    npm \
    zip unzip \
    git
RUN composer self-update --2 && npm install --global gulp-cli -y




