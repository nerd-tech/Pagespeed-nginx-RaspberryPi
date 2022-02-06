**Pagespeed-nginx-RaspberryPi**

Pagespeed Module ARM binaries compiled from source for Nginx-1.21.6 Mainline on Ubuntu Server 20.04 (Raspberry Pi 3 version). 
This uses ARM (aarch64) Specific PSOL libraries to make this module compatable with AARCH64 devices such as the Raspberry Pi 3 and Raspberry Pi 4.

**Latest Release**

The latest release of this Module was compiled from source on the Raspberry Pi 3 running Nginx 1.21.6 Mainline on Ubuntu Server 20.04 64-bit, using a aarch64 compatable PSOL from https://gitlab.com/gusco/ngx_pagespeed_arm, and distributed by www.nerd-tech.net.

**Compatability**

Hardware: Raspberry Pi 3 or Raspberry Pi 4 

Architecture: aarch64 

Compatablie Operating Systems: Ubuntu Server 20.04 (64 bit) for Raspberry Pi / Ubuntu 20.04 (64 bit) for Raspberry Pi 

Compatable Version of Nginx: Nginx 1.21.6 Mainline Binary

**Compilation Environment**

Compilation Hardware: Raspberry Pi 3 

Compilation OS: Ubuntu Server 20.04 

Compiled Against: Nginx 1.21.6 Mainline Source 

PSOL Binaries (ARM Compatable): https://gitlab.com/gusco/ngx_pagespeed_arm 

Architecture: aarch64 (64 bit ARM) 

Compiled With: Official Nginx.org Nginx-1.21.6 Mainline Source Code 

Compilation Arguements:
```
./configure --add-dynamic-module=../incubator-pagespeed-ngx --with-compat --prefix=/etc/nginx --sbin-path=/usr/sbin/nginx --modules-path=/usr/lib/nginx/modules --conf-path=/etc/nginx/nginx.conf --error-log-path=/var/log/nginx/error.log --http-log-path=/var/log/nginx/access.log --pid-path=/var/run/nginx.pid --lock-path=/var/run/nginx.lock --http-client-body-temp-path=/var/cache/nginx/client_temp --http-proxy-temp-path=/var/cache/nginx/proxy_temp --http-fastcgi-temp-path=/var/cache/nginx/fastcgi_temp --http-uwsgi-temp-path=/var/cache/nginx/uwsgi_temp --http-scgi-temp-path=/var/cache/nginx/scgi_temp --user=nginx --group=nginx --with-file-aio --with-threads --with-http_addition_module --with-http_auth_request_module --with-http_dav_module --with-http_flv_module --with-http_gunzip_module --with-http_gzip_static_module --with-http_mp4_module --with-http_random_index_module --with-http_realip_module --with-http_secure_link_module --with-http_slice_module --with-http_ssl_module --with-http_stub_status_module --with-http_sub_module --with-http_v2_module --with-mail --with-mail_ssl_module --with-stream --with-stream_realip_module --with-stream_ssl_module --with-stream_ssl_preread_module --with-cc-opt='-g -O2 -fdebug-prefix-map=/data/builder/debuild/nginx-1.21.6/debian/debuild-base/nginx-1.21.6=. -fstack-protector-strong -Wformat -Werror=format-security -Wp,-D_FORTIFY_SOURCE=2 -fPIC' --with-ld-opt='-Wl,-Bsymbolic-functions -Wl,-z,relro -Wl,-z,now -Wl,--as-needed -pie'
```
**Compatability Check**

To check if your version of Nginx is compatabile with this binary module, you should run the following commands, and 
they should return the exact same results as listed below.

`nginx -v`
```
nginx version: nginx/1.21.6
```
`nginx -V`
```
nginx version: nginx/1.21.6
built by gcc 9.3.0 (Ubuntu 9.3.0-10ubuntu2)
built with OpenSSL 1.1.1f  31 Mar 2020
TLS SNI support enabled
configure arguments: --prefix=/etc/nginx --sbin-path=/usr/sbin/nginx --modules-path=/usr/lib/nginx/modules --conf-path=/etc/nginx/nginx.conf --error-log-path=/var/log/nginx/error.log --http-log-path=/var/log/nginx/access.log --pid-path=/var/run/nginx.pid --lock-path=/var/run/nginx.lock --http-client-body-temp-path=/var/cache/nginx/client_temp --http-proxy-temp-path=/var/cache/nginx/proxy_temp --http-fastcgi-temp-path=/var/cache/nginx/fastcgi_temp --http-uwsgi-temp-path=/var/cache/nginx/uwsgi_temp --http-scgi-temp-path=/var/cache/nginx/scgi_temp --user=nginx --group=nginx --with-compat --with-file-aio --with-threads --with-http_addition_module --with-http_auth_request_module --with-http_dav_module --with-http_flv_module --with-http_gunzip_module --with-http_gzip_static_module --with-http_mp4_module --with-http_random_index_module --with-http_realip_module --with-http_secure_link_module --with-http_slice_module --with-http_ssl_module --with-http_stub_status_module --with-http_sub_module --with-http_v2_module --with-mail --with-mail_ssl_module --with-stream --with-stream_realip_module --with-stream_ssl_module --with-stream_ssl_preread_module --with-cc-opt='-g -O2 -fdebug-prefix-map=/data/builder/debuild/nginx-1.21.6/debian/debuild-base/nginx-1.21.6=. -fstack-protector-strong -Wformat -Werror=format-security -Wp,-D_FORTIFY_SOURCE=2 -fPIC' --with-ld-opt='-Wl,-Bsymbolic-functions -Wl,-z,relro -Wl,-z,now -Wl,--as-needed -pie'
```
