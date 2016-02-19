# `brew cleanup` — освобождение места на диске

Сначала проверим, сколько места можно освободить:

    $ brew cleanup -n

В вашем случае места может быть занято гораздо больше:

    $ brew cleanup -n
    Would remove: /usr/local/Cellar/diff-so-fancy/0.3.0 (4 files, 11.8K)
    Would remove: /usr/local/Cellar/go/1.5.3 (5,336 files, 259.6M)
    Would remove: /Library/Caches/Homebrew/diff-so-fancy-0.3.0.tar.gz (14.8K)
    Would remove: /Library/Caches/Homebrew/go-1.5.3.el_capitan.bottle.tar.gz (65.7M)
    ==> This operation would free approximately 325.3M of disk space.

Освобождаем место:

    $ brew cleanup
