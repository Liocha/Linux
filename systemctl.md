# systemctl

#### Вывести на экран активные сервисы и их состояние:
```
systemctl list-units -t service
```
#### Проверить состояние отдельного сервиса:
```
systemctl status mysql
```

#### Запустить сервис:
```
systemctl start mysql
```
#### Остановить:

```
systemctl stop mysql
```
#### Перезагрузить конфигурацию сервиса:

```
systemctl reload mysql
```

#### Перезапустить службу:
```
systemctl restart mysql
```
#### Перезапустить, если она запущена:
```
systemctl try-restart mysql
```
#### Выполнить reload (конфигурации), если такая команда поддеживается — или перезапустить службу. Если служба остановлена — она будет запущена:
```
systemctl reload-or-restart mysql
```

#### Убить службу:

```
systemctl kill mysql
```

#### Проверить запущен и работает ли сервис:
```
systemctl is-active mysql
active
```
#### Или с помощью кода выполнения:
```
systemctl is-active mysql; echo $?
active
0
```
```
# systemctl is-active mysql --quiet; echo $?
0
```

#### Аналогично можно проверить были ли проблемы при запуске сервиса и запущен ли он в данный момент:

```
systemctl is-failed mysql
active
```
```
systemctl is-failed mysql --quiet; echo $?
1
```
#### Если сервис был корретно остановлен:
```
systemctl is-failed mysql
inactive
```

### Управление автозапуском
#### Добавить в автозапуск:
```
systemctl enable mysql
```
#### Убрать из автозапуска:

```
systemctl disable mysql
```
#### Проверить — есть ли юнит в автозапуске:

```
systemctl is-enabled sshd
enabled
```

#### Аналогично примеру с is-active — можно использовать is-enabled:
```
systemctl is-enabled sshd
enabled
```
```
systemctl is-enabled sshd --quiet; echo $?
0
```




