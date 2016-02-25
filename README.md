# ip.aquabsd.org ![License][license-img]

## Overview

This script allow users to perform an IP address lookup.

## Description

## Requirements

You need to create simple PHP vhost pointing to `public` folder.

Example:

```
server {
  listen 80;
  server_name ip.aquabsd.org;
  root /ip.aquabsd.org/public;
  index index.php;

  location / {
    try_files $uri $uri/ /index.php;
  }

  location ~* \.php$ {
	include fastcgi.conf;
	fastcgi_pass unix:/ip.aquabsd.org.sock;
  }

  access_log /ip.aquabsd.org_access.log;
  error_log  /ip.aquabsd.org_error.log;
}
```

## Usage

```bash
$ curl http://ip.aquabsd.org/
```

# Millipede

```
    ╚⊙ ⊙╝
  ╚═(███)═╝
 ╚═(███)═╝
╚═(███)═╝
 ╚═(███)═╝
  ╚═(███)═╝
   ╚═(███)═╝
```

[license-img]: https://img.shields.io/badge/license-ISC-blue.svg
