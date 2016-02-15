# Отключение версии `nginx` в заголовках ответа

Выполняется выставлением значения директивы [`server_tokens`](http://nginx.org/ru/docs/http/ngx_http_core_module.html#server_tokens) в `off`:

    server_tokens off;

Заголовки при `server_tokens on`

    Date: Mon, 15 Feb 2016 12:41:50 GMT
    Server: nginx/1.9.11
    Transfer-Encoding: chunked

Заголовки при `server_tokens off`

    Date: Mon, 15 Feb 2016 12:39:53 GMT
    Server: nginx
    Transfer-Encoding: chunked
