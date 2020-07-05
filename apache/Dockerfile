FROM yourls:latest

RUN apt update && apt install -y \
    zlib1g-dev \
    libzip-dev

# install the PHP extensions we need
RUN set -eux; \
    docker-php-ext-install -j "$(nproc)" zip

# remove development dependencies
RUN apt remove -y \
    zlib1g-dev \
    libzip-dev
