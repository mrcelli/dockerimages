FROM nginx:1.13-alpine

MAINTAINER mrcelli

WORKDIR /var/www/html

# Ensure www-data user exists.
RUN addgroup -g 82 -S www-data \
  && adduser -u 82 -D -S -G www-data www-data

COPY nginx.conf /etc/nginx/nginx.conf
COPY drupal.conf /etc/nginx/conf.d/default.conf

ENV DOCROOT="/var/www/html" \
  SERVER_NAME="_" \
  PHP_SERVICE_NAME="php"

COPY docker-entrypoint.sh /usr/local/bin/
ENTRYPOINT ["docker-entrypoint.sh"]
CMD ["nginx", "-g", "daemon off;"]
