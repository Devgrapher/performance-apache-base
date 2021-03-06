Base Apache Docker Container for RIDI performance team
========================================================

[![](https://images.microbadger.com/badges/version/ridibooks/performance-apache-base.svg)](http://microbadger.com/images/ridibooks/performance-apache-base "Get your own version badge on microbadger.com")
[![](https://images.microbadger.com/badges/image/ridibooks/performance-apache-base.svg)](http://microbadger.com/images/ridibooks/performance-apache-base "Get your own version badge on microbadger.com")

Envionment variables
--------
- APACHE_DOC_ROOT - The document root is /var/www/html. (default) Set APACHE_DOC_ROOT if you want to change,
- XDEBUG_ENABLE - if set this "1", then XDebug is enabled.
- XDEBUG_HOST - XDebug host is computed at the start. You can specify a special host by this.
- PHP_TIMEZONE - PHP time zone. (default = Asia/Seoul)

Usage
-----

Standalone usage example with host's current working directory as document root:
```
docker run -p 80:80 \
  -v $(pwd):/var/www/html \
  --name php-apache \
  -e XDEBUG_ENABLE=1 \
  ridibooks/performance-apache-base
```