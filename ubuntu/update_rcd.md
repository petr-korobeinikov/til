# Запрет/разрешение автоматического запуска сервиса

Запретить/разрешить автозапуск сервиса можно с помощью утилиты `update-rc.d`:

    sudo update-rc.d nginx disable

или

    sudo update-rc.d nginx enable

За подробностями обращайтесь к документации: `man update-rc.d`.
