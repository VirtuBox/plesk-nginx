# Plesk Nginx

## Bash script to compile Nginx from source with additional modules

![plesk-nginx](https://raw.githubusercontent.com/VirtuBox/plesk-nginx/master/plesk-nginx.png)

## plesk-nginx [Github page](https://virtubox.github.io/plesk-nginx/) now available

**Use this script with caution and on a staging server first.**  
**Plesk or me will not be responsible if your server crash**  

-----

## Main Features

* Compile the latest Nginx mainline or stable release
* Ngx_Pagespeed
* TLS v1.3 draft 28
* Brotli
* Naxsi WAF

-----
Nginx current mainline release : **v1.15.2**  
Nginx current stable release : **v1.14.0**  

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
* Openssl 1_1_1-pre8
* ngx_brotli
* ngx_http_substitutions_filter_module
* nginx-dynamic-tls-records-patch_1.13.0
* ngx_http_auth_pam_module
* ngx_pagespeed (optional)
* [virtual-host-traffic-status](https://github.com/vozlt/nginx-module-vts)
* naxsi WAF (optional)  

-----

**Compatible Operating System :**

* Ubuntu 16.04 LTS
* Debian 8 Jessie

-----

## Usage

-----

```bash
bash <(wget -O - https://raw.githubusercontent.com/VirtuBox/plesk-nginx/master/plesk-nginx.sh)
```

-----
  
Feel free to open an issue if you have any error during the compilation.

## Nginx configuration

* My current Nginx configuration is available here : [nginx.conf](https://github.com/VirtuBox/plesk-nginx/blob/master/etc/nginx/nginx.conf)
* My SSL/TLS configuration with TLSv1.2 and TLSv1.3 is available here : [ssl.conf](https://github.com/VirtuBox/plesk-nginx/blob/master/etc/nginx/conf.d/ssl.conf)

### Roadmap

* Add examples

-----
Published & maintained by <a href="https://virtubox.net" title="VirtuBox">VirtuBox</a>
