# Поддержка `WebDAV` в `nginx`

`Nginx` из коробки (если собран с ключом `--with-http_dav_module`) имеет удобную поддержку протокола `WebDAV`,
очень простую в настройке:

    location / {
        dav_methods PUT DELETE;

        create_full_put_path on;

        limit_except GET {
            allow 192.168.1.0/32;
            deny  all;
        }
    }

Более подробно о ней можно узнать в [документации](http://nginx.org/ru/docs/http/ngx_http_dav_module.html).
