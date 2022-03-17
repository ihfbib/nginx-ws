<h1 align="center">
<br>
<img src="https://raw.githubusercontent.com/ihfbib/nginx-ws/master/nginx-ws-logo.png">
<br>
  Nginx-ws
  <br>
</h1>

<h4 align="center">
Automated Nginx compilation from sources with additional modules support
</h4>

---

<p align="center">
<a href="https://travis-ci.org/ihfbib/nginx-ws"><img src="https://travis-ci.com/ihfbib/nginx-ws.svg?branch=master" alt="build" /></a>
<img src="https://img.shields.io/github/license/ihfbib/nginx-ws.svg" alt="MIT">
<img src="https://img.shields.io/github/stars/ihfbib/nginx-ws.svg" alt="Stars">
<img src="https://img.shields.io/github/last-commit/ihfbib/nginx-ws/master.svg?style=flat" alt="Commits">
<br>
<img src="https://img.shields.io/github/release/ihfbib/nginx-ws.svg?style=flat" alt="GitHub release">
<a href="https://www.codacy.com/app/ihfbib/nginx-ws?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=ihfbib/nginx-ws&amp;utm_campaign=Badge_Grade"><img src="https://api.codacy.com/project/badge/Grade/61fe95d2311241b6b5051a04493a43c2" alt="codacy"/></a></p>



<p align="center">
<a href="#features"> Features<a> •
<a href="#additional-third-party-modules"> Modules</a> •
<a href="#compatibility"> Compatibility</a> •
<a href="#usage"> Usage</a> •
<a href="https://github.com/ihfbib/nginx-ws/wiki"> Wiki</a> •
<a href="#related"> Related</a> •
<a href="#credits"> Credits</a> •
<a href="#license"> License</a></p>

<p align="center"><img src="https://raw.githubusercontent.com/ihfbib/nginx-ws/master/nginx-ws.png" alt="nginx-ws"></p>

---

## Features

* Compile the latest Nginx releases : stable or mainline
* Install Nginx or replace Nginx package previously installed
* Nginx built-in modules selection
* Nginx Third-party modules selection
* Dynamic modules support
* Brotli Support
* TLS v1.3 support (Final)
* OpenSSL (1.1.1g or 3.0.0-dev or from system-lib) or LibreSSL
* Cloudflare HPACK
* Cloudflare zlib
* Automated nginx updates cronjob
* Compilation with GCC-7/9
* Security hardening and performance optimization enabled with proper GCC flags
* An option to omit nginx configuration, allowing usage of third party devops tools

---

## Additional Third-party modules

Nginx current mainline release : **v1.19.2**
Nginx current stable release : **v1.18.0**

* [ngx_cache_purge](https://github.com/FRiCKLE/ngx_cache_purge)
* [headers-more-nginx-module](https://github.com/openresty/headers-more-nginx-module)
* [ngx_brotli](https://github.com/google/ngx_brotli)
* [memc-nginx-module](https://github.com/openresty/memc-nginx-module.git)
* [ngx-devel-kit](https://github.com/simpl/ngx_devel_kit.git)
* [srcache-nginx-module](https://github.com/openresty/srcache-nginx-module)
* [ngx_http_substitutions_filter_module](https://github.com/yaoweibin/ngx_http_substitutions_filter_module)
* [nginx_dynamic_tls_records](https://github.com/nginx-modules/ngx_http_tls_dyn_size)
* [ipscrub](http://www.ipscrub.org/)
* [ngx_http_auth_pam_module](https://github.com/sto/ngx_http_auth_pam_module)
* [virtual-host-traffic-status](https://github.com/vozlt/nginx-module-vts)
* [Cloudflare zlib](https://github.com/cloudflare/zlib.git)
* [redis2-nginx-module](https://github.com/openresty/redis2-nginx-module.git)

For Nginx http_ssl_module :

* [OpenSSL](https://github.com/openssl/openssl)
* [LibreSSL](https://github.com/libressl-portable)

Optional modules :

* [naxsi WAF](https://github.com/nbs-system/naxsi)
* [nginx-rtmp-module](https://github.com/arut/nginx-rtmp-module)

---

## Compatibility

### Operating System

#### Recommended

* Ubuntu 20.04 LTS (Focal)
* Ubuntu 18.04 LTS (Bionic)
* Debian 10 (Buster)

#### Also compatible

* Ubuntu 19.10 (Eoan)
* Ubuntu 16.04 LTS (Xenial)
* Debian 9 (Stretch)
* Debian 8 (Jessie)
* Raspbian 9 (Stretch)
* Raspbian 10 (Buster)

### Applications

#### LEMP Stack

* EasyEngine v3
* WordOps

#### Plesk

* 17.5.x (Onyx)
* 17.8.x
* 17.9.x
* 18.x (Obsidian)

---

## Usage

### One-Step Automated Install

**Default settings** :

* mainline release
* openssl stable : 1.1.1g
* without naxsi
* without rtmp

```bash
bash <(wget -qO - rd.wooserv.com/nginx-ws || curl -sL rd.wooserv.com/nginx-ws)
```

### Alternative Install Method

```bash
git clone https://github.com/ihfbib/nginx-ws
cd nginx-ws
sudo bash nginx-build.sh
```

### Interactive install

Interactive installation is available with arguments `-i` or `--interactive`

```bash
bash <(wget -O - rd.wooserv.com/nginx-ws || curl -sL rd.wooserv.com/nginx-ws) --interactive
```

### Custom installation

Example : Nginx stable release with naxsi

```bash
bash <(wget -O - rd.wooserv.com/nginx-ws || curl -sL rd.wooserv.com/nginx-ws) --stable --naxsi
```

#### Options available

Nginx build options :

* `--stable` : compile Nginx stable release
* `--full` : Naxsi + RTMP
* `--dynamic` : Compile Nginx modules as dynamic modules
* `--noconf` : Compile Nginx without any configuring. Useful when you use devops tools like ansible.

Optional third-party modules :

* `--naxsi` : compile nginx with naxsi
* `--rtmp` : compile nginx with rtmp module
* `--libressl` : compile nginx with LibreSSL instead of OpenSSL
* `--openssl-dev` : compile nginx with OpenSSL 3.0.0-dev
* `--openssl-system` : compile nginx with OpenSSL system lib

Extras :

* `--cron` : setup daily cronjob to update nginx each time a new release is available

---

## Roadmap

* [x] Add choice between stable & mainline release
* [x] Add Nginx configuration examples
* [x] Add Cloudflare HPACK patch
* [x] Add support for servers without EasyEngine
* [x] Add non-interactive installation
* [x] Add automated update detection
* [x] Add support for Plesk servers
* [x] Add Nginx modules choice
* [x] Add support for Debian 9
* [x] Add openssl release choice
* [x] Add more compilation presets
* [x] Add support for LibreSSL
* [x] Add noconf support
* [ ] Add support for config.inc build configuration
* [ ] Add HTTP/3 QUIC support

---

## Contributing

If you have any ideas, just open an issue and describe what you would like to add/change in Nginx-ee.

If you'd like to contribute, please fork the repository and make changes as you'd like. Pull requests are warmly welcome.

## Credits

* [centminmod](https://github.com/centminmod/centminmod) : Nginx, Nginx modules & various other patches
* [hakase](https://github.com/hakasenyang/openssl-patch) : OpenSSL-patch
* [Karl Chen](https://github.com/kn007/patch) : Nginx patches

## License

[MIT](https://github.com/ihfbib/nginx-ws/blob/master/LICENSE) © <a href="https://www.wooserv.com" title="WooServ" target="_blank">WooServ</a>
