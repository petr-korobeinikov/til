# .pgpass — файл паролей

Файл паролей `.pgpass` позволяет не вводить пароль при соединении с базой данных.

Он должен находиться в домашнем каталоге или по пути, заданному переменной `PGPASSFILE`, и имеет следующий формат:

    hostname1:port:database1:username1:password1
    hostname2:port:database2:username2:password2
    hostname3:port:database3:username3:password3
    ...

Необходимо, чтобы на `.pgpass` были установлены права доступа `0600`:

    chmod 0600 ~/.pgpass

Документация: [http://www.postgresql.org/docs/current/static/libpq-pgpass.html](http://www.postgresql.org/docs/current/static/libpq-pgpass.html)
