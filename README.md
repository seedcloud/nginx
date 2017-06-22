# Nginx docker container image

This repository was forked initially from https://github.com/wodby/nginx

## Supported tags and respective `Dockerfile` links

- [`1.13-2.2.0`, `1.13`, `latest` (*1.13/Dockerfile*)](https://github.com/seedcloud/nginx/tree/master/1.13/Dockerfile)
- [`1.12-2.2.0`, `1.12`, `stable` (*1.12/Dockerfile*)](https://github.com/seedcloud/nginx/tree/master/1.12/Dockerfile)

## Environment variables available for customization

| Environment Variable | Default Value | Description |
| -------------------- | ------------- | ----------- |
| NGINX_ACCESS_LOG               | /proc/self/fd/2       | |
| NGINX_BACKEND_HOST             |                       | |
| NGINX_BACKEND_PORT             | 9000                  | |
| NGINX_CLIENT_BODY_TIMEOUT      | 600                   | |
| NGINX_CLIENT_HEADER_TIMEOUT    | 600                   | |
| NGINX_CLIENT_MAX_BODY_SIZE     | 256                   | |
| NGINX_CONF_INCLUDE             | conf.d/*.conf         | |
| NGINX_ERROR_LOG                | /proc/self/fd/2       | |
| NGINX_ERROR_LOG_LEVEL          | error                 | |
| NGINX_FASTCGI_BUFFERS          | 16 32k                | |
| NGINX_FASTCGI_BUFFER_SIZE      | 32k                   | |
| NGINX_FASTCGI_INTERCEPT_ERRORS | on                    | |
| NGINX_FASTCGI_READ_TIMEOUT     | 900                   | |
| NGINX_GZIP                     | on                    | |
| NGINX_GZIP_BUFFERS             | 16 8k                 | |
| NGINX_GZIP_COMP_LEVEL          | 2                     | |
| NGINX_GZIP_DISABLE             | msie6                 | |
| NGINX_GZIP_HTTP_VERSION        | 1.1                   | |
| NGINX_GZIP_MIN_LENGTH          | 20                    | |
| NGINX_GZIP_PROXIED             | any                   | |
| NGINX_GZIP_VARY                | on                    | |
| NGINX_KEEPALIVE_REQUESTS       | 100                   | |
| NGINX_KEEPALIVE_TIMEOUT        | 60                    | |
| NGINX_MULTI_ACCEPT             | on                    | |
| NGINX_RESET_TIMEOUT_CONNECTION | off                   | |
| NGINX_SEND_TIMEOUT             | 600                   | |
| NGINX_SENDFILE                 | on                    | |
| NGINX_SERVER_NAME              | default               | |
| NGINX_SERVER_TOKENS            | off                   | |
| NGINX_TCP_NODELAY              | on                    | |
| NGINX_TCP_NOPUSH               | on                    | |
| NGINX_UPLOAD_PROGRESS          | uploads 1m            | |
| NGINX_WORKER_CONNECTIONS       | 1024                  | |
| NGINX_WORKER_PROCESSES         | auto                  | |

## Actions

Usage:
```
make COMMAND [params ...]

commands:
    check-ready [host max_try wait_seconds delay_seconds]

default params values:
    host localhost
    max_try 1
    wait_seconds 1
    delay_seconds 0
```

Examples:

```bash
# Wait for Nginx to start
docker exec -ti [ID] make check-ready max_try=10 -f /usr/local/bin/actions.mk
```
