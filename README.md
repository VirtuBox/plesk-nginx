### Plesk Onyx Nginx from source with TLS 1.3 Support + Brotli and other additional modules

This is a script to compile nginx from source with some additional modules. It was currently tested on Ubuntu 16.04 LTS and on Centos 7.
Feel free to open an issue if you have any error during the compilation.

**Use this script with caution and on a staging server first. Plesk or me will not be responsible if your server crash**

-----
Nginx current version : 1.13.7

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
* nginx-dynamic-tls-records-patch_1.11.5
* ngx_pagespeed (optional)
-----

## Compile Nginx
-----
**Ubuntu/Debian**

Without pagespeed
```
bash <(wget -O - https://raw.githubusercontent.com/VirtuBox/plesk-nginx/master/nginx/build-deb.sh)
```

With pagespeed
```
bash <(wget -O - https://raw.githubusercontent.com/VirtuBox/plesk-nginx/master/nginx/build-deb-pagespeed.sh)
```
-----

**Centos/Redhat**
```
bash <(wget -O - https://raw.githubusercontent.com/VirtuBox/plesk-nginx/master/nginx/build-rpm.sh)
```

## Nginx configuration

My current Nginx configuration is available here : [nginx.conf](https://github.com/VirtuBox/plesk-nginx/blob/master/etc/nginx/nginx.conf)
And my SSL/TLS configuration with TLSv1.2 and TLSv1.3 is available here : [nginx.conf](https://github.com/VirtuBox/plesk-nginx/blob/master/etc/nginx/conf.d/ssl.conf)

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


