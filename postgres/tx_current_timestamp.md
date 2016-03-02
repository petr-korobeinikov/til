# `now()` и `current_timestamp` возвращают время старта транзакции

Чтобы получить текущее время внутри транзакции, используйте функцию `clock_timestamp()`:

    begin;
    select now(), current_timestamp, clock_timestamp();
    select pg_sleep(5);
    select now(), current_timestamp, clock_timestamp();
    commit;
