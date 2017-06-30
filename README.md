Nginx-1.10.1 with custom packages
===================

below are nginx build with custom modules to support extra funtionality. version of nginx (Ver. 1.10.1) complied with google pagespeed module (Ver. 1.11.33.2) and http perl module to support regex in nginx configurations.

----------
> **Nginx**

> - nginx_1.10.1-1~trusty_amd64.deb. -- base package
> - nginx-module-geoip_1.10.1-1~trusty_amd64.deb - [nginx geoip module](http://nginx.org/en/docs/http/ngx_http_geoip_module.html).
> - nginx-module-image-filter_1.10.1-1~trusty_amd64.deb - [nginx image filter module](http://nginx.org/en/docs/http/ngx_http_image_filter_module.html).
> - nginx-module-njs_1.10.1.0.0.20160414.1c50334fbea6-1~trusty_amd64.deb - [nginx nginScript](https://www.nginx.com/resources/wiki/nginScript/) .
> - nginx-module-perl_1.10.1-1~trusty_amd64.deb - [nginx perl module](http://nginx.org/en/docs/http/ngx_http_perl_module.html).
> - nginx-module-xslt_1.10.1-1~trusty_amd64.deb - [nginx xslt module](http://nginx.org/en/docs/http/ngx_http_xslt_module.html).

**step to hold package from auto upgrade**
```
sudo set on hold nginx
apt-mark showhold
echo "nginx hold" | sudo dpkg --set-selections
dpkg --get-selections | grep 'hold$'
sudo apt-mark hold nginx
```
