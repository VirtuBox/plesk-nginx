# Compile the latest nginx mainline release for Plesk Onyx

This script compile the latest nginx mailine release from source with additional modules with Plesk Onyx. <br>

Feel free to open an issue if you have any error during the compilation.
**Use this script with caution and on a staging server first. Plesk or me will not be responsible if your server crash**

-----
Nginx current version : **v1.13.9**

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
* ngx_brotli
* ngx_http_substitutions_filter_module
* nginx-dynamic-tls-records-patch_1.13.0+
* ngx_http_auth_pam_module
* ngx_pagespeed (optional)
* naxsi WAF (optional)
-----

**Compatible Operating System :**
* Ubuntu 16.04 LTS
* Debian 8 Jessie

-----

## Usage 
-----

```
bash <(wget -O - https://raw.githubusercontent.com/VirtuBox/plesk-nginx/master/plesk-nginx.sh)
```
![plesk-nginx](https://raw.githubusercontent.com/VirtuBox/plesk-nginx/master/plesk-nginx.png)

-----

## Nginx configuration

* My current Nginx configuration is available here : [nginx.conf](https://github.com/VirtuBox/plesk-nginx/blob/master/etc/nginx/nginx.conf)
* My SSL/TLS configuration with TLSv1.2 and TLSv1.3 is available here : [ssl.conf](https://github.com/VirtuBox/plesk-nginx/blob/master/etc/nginx/conf.d/ssl.conf)

### Roadmap

- Add nginx stable relase 
- Add examples 

-----
Published by <a href="https://virtubox.net" title="VirtuBox">VirtuBox</a>

