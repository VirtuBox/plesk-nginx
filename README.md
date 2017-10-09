### Plesk Onyx Nginx from source with TLS 1.3 Support + Brotli and other additional modules

This is a script to compile nginx from source with some additional modules. It was tested on Ubuntu 16.04 LTS.
Feel free to open an issue if you have any error during the compilation.

-----

others modules included :
* ngx_cache_purge
* memc-nginx-module
* headers-more-nginx-module
* ngx_devel_kit
* echo-nginx-module
* redis2-nginx-module
* ngx_http_redis-0.3.8
* srcache-nginx-modul
* set-misc-nginx-module
* ngx_coolkit
* ngx_slowfs_cache
* ngx_http_substitutions_filter_module
* nginxdynamic_tls_records_1.11.5

To run the script
```
bash <(wget --no-check-certificate -O - https://raw.githubusercontent.com/VirtuBox/plesk-nginx/master/nginx/build.sh)
```


