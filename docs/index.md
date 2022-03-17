﻿---
title: Nginx-ee - Automated Nginx compilation from sources with additional modules support
layout: default
---

<h1 align="center">
<br>
<img src="https://raw.githubusercontent.com/ihfbib/nginx-ws/master/nginx-ws-logo.png" alt="nginx-ws">
<br>
  Nginx-ee
  <br>
</h1>
<h4 align="center">
Automated Nginx compilation from sources with additional modules support
</h4>
<hr />
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
<a href="#license"> License</a>
<p align="center"><img src="https://raw.githubusercontent.com/ihfbib/nginx-ws/master/nginx-ws.png" alt="nginx-ws"></p>
<hr />
<h2 id="features">Features</h2>
<ul>
<li>Compile the latest Nginx releases : stable or mainline</li>
<li>Install Nginx or replace Nginx package previously installed</li>
<li>Nginx built-in modules selection</li>
<li>Nginx Third-party modules selection</li>
<li>Dynamic modules support</li>
<li>Brotli Support</li>
<li>TLS v1.3 support (Final)</li>
<li>OpenSSL (1.1.1g or 3.0.0-dev or from system-lib) or LibreSSL</li>
<li>Cloudflare HPACK</li>
<li>Cloudflare zlib</li>
<li>Automated nginx updates cronjob</li>
<li>Compilation with GCC-7/9</li>
<li>Security hardening and performance optimization enabled with proper GCC flags</li>
</ul>
<hr />
<h2 id="additional-third-party-modules">Additional Third-party modules</h2>
<p>Nginx current mainline release : <strong>v1.19.2</strong>
Nginx current stable release : <strong>v1.18.0</strong></p>
<ul>
<li><a href="https://github.com/FRiCKLE/ngx_cache_purge">ngx_cache_purge</a></li>
<li><a href="https://github.com/openresty/headers-more-nginx-module">headers-more-nginx-module</a></li>
<li><a href="https://github.com/google/ngx_brotli">ngx_brotli</a></li>
<li><a href="https://github.com/openresty/memc-nginx-module.git">memc-nginx-module</a></li>
<li><a href="https://github.com/simpl/ngx_devel_kit.git">ngx-devel-kit</a></li>
<li><a href="https://github.com/openresty/srcache-nginx-module">srcache-nginx-module</a></li>
<li><a href="https://github.com/yaoweibin/ngx_http_substitutions_filter_module">ngx_http_substitutions_filter_module</a></li>
<li><a href="https://github.com/nginx-modules/ngx_http_tls_dyn_size">nginx_dynamic_tls_records</a></li>
<li><a href="http://www.ipscrub.org/">ipscrub</a></li>
<li><a href="https://github.com/sto/ngx_http_auth_pam_module">ngx_http_auth_pam_module</a></li>
<li><a href="https://github.com/vozlt/nginx-module-vts">virtual-host-traffic-status</a></li>
<li><a href="https://github.com/cloudflare/zlib.git">Cloudflare zlib</a></li>
<li><a href="https://github.com/openresty/redis2-nginx-module.git">redis2-nginx-module</a></li>
</ul>
<p>For Nginx http_ssl_module :</p>
<ul>
<li><a href="https://github.com/openssl/openssl">OpenSSL</a></li>
<li><a href="https://github.com/libressl-portable">LibreSSL</a></li>
</ul>
<p>Optional modules :</p>
<ul>
<li><a href="https://github.com/apache/incubator-pagespeed-ngx">ngx_pagespeed</a></li>
<li><a href="https://github.com/nbs-system/naxsi">naxsi WAF</a></li>
<li><a href="https://github.com/arut/nginx-rtmp-module">nginx-rtmp-module</a></li>
</ul>
<hr />
<h2 id="compatibility">Compatibility</h2>
<h3 id="operating-system">Operating System</h3>
<h4 id="recommended">Recommended</h4>
<ul>
<li>Ubuntu 20.04 LTS (Focal)</li>
<li>Ubuntu 18.04 LTS (Bionic)</li>
<li>Debian 10 (Buster)</li>
</ul>
<h4 id="also-compatible">Also compatible</h4>
<ul>
<li>Ubuntu 19.10 (Eoan)</li>
<li>Ubuntu 19.04 (Disco)</li>
<li>Ubuntu 18.10 (Cosmic)</li>
<li>Ubuntu 16.04 LTS (Xenial)</li>
<li>Debian 9 (Stretch)</li>
<li>Debian 8 (Jessie)</li>
<li>Raspbian 9 (Stretch)</li>
<li>Raspbian 10 (Buster)</li>
</ul>
<h3 id="applications">Applications</h3>
<h4 id="lemp-stack">LEMP Stack</h4>
<ul>
<li>EasyEngine v3</li>
<li>WordOps</li>
</ul>
<h4 id="plesk">Plesk</h4>
<ul>
<li>17.5.x</li>
<li>17.8.x</li>
<li>17.9.x</li>
<li>18.x (Obsidian)</li>
</ul>
<hr />
<h2 id="usage">Usage</h2>
<h3 id="one-step-automated-install">One-Step Automated Install</h3>
<p><strong>Default settings</strong> :</p>
<ul>
<li>mainline release</li>
<li>openssl stable : 1.1.1g</li>
<li>without pagespeed</li>
<li>without naxsi</li>
<li>without rtmp</li>
</ul>
<pre><code class="language-bash">bash &lt;(wget -O - git.wooserv.com/nginx-ws || curl -sL git.wooserv.com/nginx-ws)
</code></pre>
<h3 id="alternative-install-method">Alternative Install Method</h3>
<pre><code class="language-bash">git clone https://github.com/ihfbib/nginx-ws
cd nginx-ws
sudo bash nginx-build.sh
</code></pre>
<h3 id="interactive-install">Interactive install</h3>
<p>Interactive installation is available with arguments <code>-i</code> or <code>--interactive</code></p>
<pre><code class="language-bash">bash &lt;(wget -O - git.wooserv.com/nginx-ws || curl -sL git.wooserv.com/nginx-ws) --interactive
</code></pre>
<h3 id="custom-installation">Custom installation</h3>
<p>Example : Nginx stable release with pagespeed and naxsi</p>
<pre><code class="language-bash">bash &lt;(wget -O - git.wooserv.com/nginx-ws || curl -sL git.wooserv.com/nginx-ws) --stable --pagespeed --naxsi
</code></pre>
<h4 id="options-available">Options available</h4>
<p>Nginx build options :</p>
<ul>
<li><code>--stable</code> : compile Nginx stable release</li>
<li><code>--full</code> : Naxsi + PageSpeed + RTMP</li>
<li><code>--dynamic</code> : Compile Nginx modules as dynamic modules</li>
</ul>
<p>Optional third-party modules :</p>
<ul>
<li><code>--pagespeed</code>: compile nginx with ngx_pagespeed latest-stable</li>
<li><code>--pagespeed-beta</code>: compile nginx with ngx_pagespeed latest-beta</li>
<li><code>--naxsi</code> : compile nginx with naxsi</li>
<li><code>--rtmp</code> : compile nginx with rtmp module</li>
<li><code>--libressl</code> : compile nginx with LibreSSL instead of OpenSSL</li>
<li><code>--openssl-dev</code> : compile nginx with OpenSSL 3.0.0-dev</li>
<li><code>--openssl-system</code> : compile nginx with OpenSSL system lib</li>
</ul>
<p>Extras :</p>
<ul>
<li><code>--cron</code> : setup daily cronjob to update nginx each time a new release is available</li>
</ul>
<hr />
<h2 id="roadmap">Roadmap</h2>
<ul class="contains-task-list">
<li class="task-list-item"><input disabled="disabled" type="checkbox" checked="checked" /> Add choice between stable &amp; mainline release</li>
<li class="task-list-item"><input disabled="disabled" type="checkbox" checked="checked" /> Add Nginx configuration examples</li>
<li class="task-list-item"><input disabled="disabled" type="checkbox" checked="checked" /> Add Cloudflare HPACK patch</li>
<li class="task-list-item"><input disabled="disabled" type="checkbox" checked="checked" /> Add support for servers without EasyEngine</li>
<li class="task-list-item"><input disabled="disabled" type="checkbox" checked="checked" /> Add non-interactive installation</li>
<li class="task-list-item"><input disabled="disabled" type="checkbox" checked="checked" /> Add automated update detection</li>
<li class="task-list-item"><input disabled="disabled" type="checkbox" checked="checked" /> Add support for Plesk servers</li>
<li class="task-list-item"><input disabled="disabled" type="checkbox" checked="checked" /> Add Nginx modules choice</li>
<li class="task-list-item"><input disabled="disabled" type="checkbox" checked="checked" /> Add support for Debian 9</li>
<li class="task-list-item"><input disabled="disabled" type="checkbox" /> Add support for config.inc build configuration</li>
<li class="task-list-item"><input disabled="disabled" type="checkbox" checked="checked" /> Add openssl release choice</li>
<li class="task-list-item"><input disabled="disabled" type="checkbox" checked="checked" /> Add more compilation presets</li>
<li class="task-list-item"><input disabled="disabled" type="checkbox" checked="checked" /> Add support for LibreSSL</li>
</ul>
<hr />

<h2 id="contributing">Contributing</h2>
<p>If you have any ideas, just open an issue and describe what you would like to add/change in Nginx-ee.</p>
<p>If you'd like to contribute, please fork the repository and make changes as you'd like. Pull requests are warmly welcome.</p>
<h2 id="credits">Credits</h2>
<ul>
<li><a href="https://github.com/centminmod/centminmod">centminmod</a> : Nginx, Nginx modules &amp; various other patches</li>
<li><a href="https://github.com/hakasenyang/openssl-patch">hakase</a> : OpenSSL-patch</li>
<li><a href="https://github.com/kn007/patch">Karl Chen</a> : Nginx patches</li>
</ul>
<h2 id="license">License</h2>
<p><a href="https://github.com/ihfbib/nginx-ws/blob/master/LICENSE">MIT</a> © <a href="https://www.wooserv.com" title="WooServ" target="_blank">WooServ</a></p>
