# dl-1c
Скрипт для скачивания релизов с сайта releases.1c.ru

---
## Использование

```
executor.cmd -s dl-1c.sbsl username password target version
```

- `username` - имя пользователя
- `password` - пароль пользователя
- `target` - цель для скачивания (см. ниже)
- `version` - версия цели для скачивания (как на сайте, см. примеры)

### Цель для скачивания (`target`)

Значение        | Расшифровка
-|-
platform-win64  | Технологическая платформа 1С:Предприятия (64-bit) для Windows
platform-win32  | Технологическая платформа 1С:Предприятия для Windows
server-win64    | Cервер 1С:Предприятия (64-bit) для Windows
server-deb64    | Cервер 1С:Предприятия (64-bit) для DEB-based Linux-систем
thinclient-win64| Тонкий клиент 1С:Предприятие (64-bit) для Windows
thinclient-win32| Тонкий клиент 1С:Предприятия для Windows
postgres-win    | Дистрибутив СУБД PostgreSQL для Windows (64-bit) одним архивом
postgres-deb    | Дистрибутив СУБД PostgreSQL для Linux x86 (64-bit) одним архивом (DEB)
config-*        | Полная конфигурация
update-*        | Обновление конфигурации

Для целей `config-*` и `update-*` вместо `*` указывается тег конфигурации (см. URL перехода на странице с таблицей всех релизов)

### Примеры

```
executor.cmd -s dl-1c.sbsl 77777-77 pasw0rd platform-win64 8.3.17.1496
executor.cmd -s dl-1c.sbsl 77777-77 pasw0rd postgres-deb 11.7-5.1C
executor.cmd -s dl-1c.sbsl 77777-77 pasw0rd config-SSL31 3.1.3.179
executor.cmd -s dl-1c.sbsl 77777-77 pasw0rd update-HRM30 3.1.14.61
```

### Проблемы

Из-за [ошибки](https://github.com/klimenko-1c/dl-1c/issues/1) в (текущей) 2020.2.0.547 версии 1С:Исполнителя эта штука не работает :(
