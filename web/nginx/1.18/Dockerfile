FROM nginx:1.18-alpine

MAINTAINER mrcelli

WORKDIR /var/www/html

# Ensure www-data user exists.
RUN adduser -D -H -u 1000 -s /bin/bash www-data -G www-data

COPY nginx.conf /etc/nginx/nginx.conf
COPY drupal.conf /etc/nginx/conf.d/default.conf

ENV DOCROOT="/var/www/html" \
  SERVER_NAME="_" \
  PHP_SERVICE_NAME="php"

COPY docker-entrypoint.sh /usr/local/bin/
ENTRYPOINT ["docker-entrypoint.sh"]
CMD ["nginx", "-g", "daemon off;"]
