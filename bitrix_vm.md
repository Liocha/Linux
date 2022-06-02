bitrix vm

1. Скрипт меню это menu.sh Вызов в файле .bash_profile

2. Чтобы вручную включить нужное расширение, нужно файл {имя_расширения}.ini.disabled переименовать в {имя_расширения}.ini и перезапустить сервис Apache – httpd.

```bash
/etc/php.d/
mv 20-xmlwriter.ini.disabled 20-xmlwriter.ini
```
