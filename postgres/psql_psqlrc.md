# `.psqlrc` — rc-скрипт для `psql`

Этот файл читается при каждом запуске `psql` (если не указаны флаги `-c`, `--no-psqlrc` или `-X`)
и может содержать найстройку приглашения командной строки и пользовательские алиасы.

Например, так выглядит мой `.psqlrc`:

    -- Tab completion in uppercase.
    \set COMP_KEYWORD_CASE lower

    -- Switch to expanded table format automatically.
    \x auto

    -- Prompt: user @ database conn_status is_transaction
    -- todo: use %p after 9.5 release for backend pid
    SELECT pg_catalog.pg_backend_pid() AS backend_pid \gset
    \set PROMPT1 '%n@%/%R%(%:backend_pid:)#%x '

    \pset null 'Ø'

    -- Turn on timing.
    \timing
