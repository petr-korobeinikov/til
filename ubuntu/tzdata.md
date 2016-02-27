# Неинтерактивная конфигурация `tzdata`

Часто бывает необходимо переконфигурировать настройки `Ubuntu\Debian` в неинтерактивном режиме.
Это позволяет сделать ключ `-f noninteractive` команды `dpkg-reconfigure`.
Вот как это может выглядеть на примере конфигурации `tzdata`:

    $ echo -e "Europe/Moscow\n" > /etc/timezone
    $ dpkg-reconfigure -f noninteractive tzdata

Такой фрагмент `ansible playbook` я использую для автоматизированной настройки `tzdata` на серверах:

    ---
    - name: update tzdata
      copy: content="Europe/Moscow\n" dest=/etc/timezone owner=root group=root mode=0644
      register: timezone

    - name: reconfigure tzdata
      shell: dpkg-reconfigure -f noninteractive tzdata
      when: timezone.changed
