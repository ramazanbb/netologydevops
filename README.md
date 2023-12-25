# Домашнее задание к занятию "`Система мониторинга Zabbix`" - `Рамазанов Бакит`

### Задание 1
Установите Zabbix Server с веб-интерфейсом.

Процесс выполнения
1. Выполняя ДЗ, сверяйтесь с процессом отражённым в записи лекции.
2. Установите PostgreSQL. Для установки достаточна та версия, что есть в системном репозитороии Debian 11.
3. Пользуясь конфигуратором команд с официального сайта, составьте набор команд для установки последней версии Zabbix с поддержкой PostgreSQL и Apache.
4. Выполните все необходимые команды для установки Zabbix Server и Zabbix Web Server.

Требования к результаты
1. Прикрепите в файл README.md скриншот авторизации в админке.
2. Приложите в файл README.md текст использованных команд в GitHub.
 
### Решение 1
Скрин админки
![alt text](https://github.com/ramazanbb/netologydevops/blob/main/img/админка.png)

команды

установка postgresql

```sudo apt install ```

установка репозитория Zabbix

``` wget https://repo.zabbix.com/zabbix/6.4/debian/pool/main/z/zabbix-release/zabbix-release_6.4-1+debian11_all.deb

 dpkg -i zabbix-release_6.4-1+debian11_all.deb
 
 apt update ```
 
установка Zabbix сервера, веб-интерфейас и агента

``` apt install zabbix-server-pgsql zabbix-frontend-php php7.4-pgsql zabbix-apache-conf zabbix-sql-scripts zabbix-agent ```

Создание базы данных

``` sudo -u postgres createuser --pwprompt zabbix

 sudo -u postgres createdb -O zabbix zabbix ```
 
Настройте базу данных для Zabbix сервера

``` nano /etc/zabbix/zabbix_server.conf ```

Запуск процессов Zabbix сервера и агента

``` systemctl restart zabbix-server zabbix-agent apache2

 systemctl enable zabbix-server zabbix-agent apache2 ```

---

### Задание 2

Установите Zabbix Agent на два хоста.

Процесс выполнения:
1. Выполняя ДЗ, сверяйтесь с процессом отражённым в записи лекции.
2. Установите Zabbix Agent на 2 вирт.машины, одной из них может быть ваш Zabbix Server.
3. Добавьте Zabbix Server в список разрешенных серверов ваших Zabbix Agentов.
4. Добавьте Zabbix Agentов в раздел Configuration > Hosts вашего Zabbix Servera.
5. Проверьте, что в разделе Latest Data начали появляться данные с добавленных агентов.
Требования к результаты
1. Приложите в файл README.md скриншот раздела Configuration > Hosts, где видно, что агенты подключены к серверу
2. Приложите в файл README.md скриншот лога zabbix agent, где видно, что он работает с сервером
3. Приложите в файл README.md скриншот раздела Monitoring > Latest data для обоих хостов, где видны поступающие от агентов данные.
4. Приложите в файл README.md текст использованных команд в GitHub


### Решение 2

---
## Дополнительные задания (со звездочкой*)

Эти задания дополнительные (не обязательные к выполнению) и никак не повлияют на получение вами зачета по этому домашнему заданию. Вы можете их выполнить, если хотите глубже и/или шире разобраться в материале.

### Задание 3 
Установите Zabbix Agent на Windows (компьютер) и подключите его к серверу Zabbix.
Требования к результаты
1. Приложите в файл README.md скриншот раздела Latest Data, где видно свободное место на диске C:

