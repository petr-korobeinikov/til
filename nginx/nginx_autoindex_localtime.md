# Вывод локального времени в `autoindex`

Директива [`autoindex_localtime`](http://nginx.org/ru/docs/http/ngx_http_autoindex_module.html#autoindex_localtime) позволяет выводить локальное время вместо `UTC` в листингах `location`-ов, для которых включен `autoindex`:

    autoindex_localtime on;

