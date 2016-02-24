# Базовая информация о статусе сервера

У `nginx` есть модуль [`ngx_http_stub_status_module`](http://nginx.org/ru/docs/http/ngx_http_stub_status_module.html), который предоставляет доступ к базовой информации о состоянии сервера.

    location /basic_status {
        stub_status;
    }

Более мощный [`ngx_http_status_module`](http://nginx.org/ru/docs/http/ngx_http_status_module.html) доступен как часть коммерческой подписки.
