# Compile the latest nginx mainline release for Plesk Onyx

This is a script to compile the latest nginx mailine release from source with some additional modules. <br>
Tested & Working fine on Ubuntu 16.04 LTS. A script for Centos 7 is available on [Plesk community resources](https://talk.plesk.com/resources/script-for-building-replacement-of-default-sw-nginx-plesk-package-centos7-only.5/)<br>
Feel free to open an issue if you have any error during the compilation.

**Use this script with caution and on a staging server first. Plesk or me will not be responsible if your server crash**

-----
Nginx current version : 1.13.8

others modules included :
* ngx_cache_purge
* memc-nginx-module
* headers-more-nginx-module
* ngx_devel_kit
* echo-nginx-module
* redis2-nginx-module
* ngx_http_redis-0.3.8
* srcache-nginx-module
* set-misc-nginx-module
* ngx_coolkit
* ngx_brotli
* ngx_slowfs_cache
* ngx_http_substitutions_filter_module
* nginx-dynamic-tls-records-patch_1.13.0+
* ngx_http_auth_pam_module
* ngx_pagespeed (optional)
-----

## Compile Nginx
-----

Without pagespeed
```
bash <(wget -O - https://raw.githubusercontent.com/VirtuBox/plesk-nginx/master/nginx/build-deb.sh)
```

With pagespeed
```
bash <(wget -O - https://raw.githubusercontent.com/VirtuBox/plesk-nginx/master/nginx/build-deb-pagespeed.sh)
```
-----

## Nginx configuration

* My current Nginx configuration is available here : [nginx.conf](https://github.com/VirtuBox/plesk-nginx/blob/master/etc/nginx/nginx.conf)
* My SSL/TLS configuration with TLSv1.2 and TLSv1.3 is available here : [ssl.conf](https://github.com/VirtuBox/plesk-nginx/blob/master/etc/nginx/conf.d/ssl.conf)

You can apply the same configuration witht the command  : 
```
wget -O /etc/nginx/nginx.conf https://raw.githubusercontent.com/VirtuBox/plesk-nginx/master/etc/nginx/nginx.conf
wget -O /etc/nginx/conf.d/ssl.conf https://raw.githubusercontent.com/VirtuBox/plesk-nginx/master/etc/nginx/conf.d/ssl.conf
nginx -t
sudo systemctl restart nginx
```

### Features available Soon

- Add menu to choose modules
- custom nginx example configuration for redis-cache, headers etc ...


