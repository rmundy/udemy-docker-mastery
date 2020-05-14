# create your custom drupal image here, based of official drupal
# create your drupal and postgres config here, based off the last assignment
FROM drupal:8.6

RUN apt-get update && apt-get install -y git \
    && rn -rf /var/lib/apt/lists/*

WORKDIR /var/www/html/themes

RUN git clone --branch 8.x-3.x --single-branch --depth 1 https://git.drupal.org/project/bootstrap.git \
    && chown -R www-data:www-data bootstrap

WORKDIR /var/www/html