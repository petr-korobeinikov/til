# Использование `heredoc`

Иногда бывает необходимо подать несколько строк на вход некоторой команды.

Для этого можно использовать `heredoc`, например:

    cat <<EOF
    hello
    multiline
    input
    aka heredoc
    EOF
