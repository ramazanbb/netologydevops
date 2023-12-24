# Домашнее задание к занятию "`Что такое DevOps. СI/СD`" - `Рамазанов Бакит`

### Задание 1

`Что нужно сделать:`

1. `Установите себе jenkins по инструкции из лекции или любым другим способом из официальной документации. Использовать Docker в этом задании нежелательно.`
2. `Установите на машину с jenkins golang.`
3. `Используя свой аккаунт на GitHub, сделайте себе форк репозитория. В этом же репозитории находится дополнительный материал для выполнения ДЗ.`
4. `Создайте в jenkins Freestyle Project, подключите получившийся репозиторий к нему и произведите запуск тестов и сборку проекта go test . и docker build .`
В качестве ответа пришлите скриншоты с настройками проекта и результатами выполнения сборки.
 
### Решение 1
Настройки
![alt text](https://github.com/ramazanbb/netologydevops/blob/main/img/2023-12-24_15-47-38.png)
результат сборки
![alt text](https://github.com/ramazanbb/netologydevops/blob/main/img/2023-12-24_15-48-34.png)

---

### Задание 2

`Что нужно сделать:`

1. `Создайте новый проект pipeline.`
2. `Перепишите сборку из задания 1 на declarative в виде кода.`
В качестве ответа пришлите скриншоты с настройками проекта и результатами выполнения сборки.

### Решение 2
![alt text](img/2.1.png)
![alt text](img/1.1.png)
---

### Задание 3

`Что нужно сделать:`

1. `Установите на машину Nexus.`
2. `Создайте raw-hosted репозиторий.`
3. `Измените pipeline так, чтобы вместо Docker-образа собирался бинарный go-файл. Команду можно скопировать из Dockerfile.`
4. `Загрузите файл в репозиторий с помощью jenkins.`
В качестве ответа пришлите скриншоты с настройками проекта и результатами выполнения сборки.

### Решение 3


---
## Дополнительные задания (со звездочкой*)

Эти задания дополнительные (не обязательные к выполнению) и никак не повлияют на получение вами зачета по этому домашнему заданию. Вы можете их выполнить, если хотите глубже и/или шире разобраться в материале.

### Задание 4 

`Придумайте способ версионировать приложение, чтобы каждый следующий запуск сборки присваивал имени файла новую версию. Таким образом, в репозитории Nexus будет храниться история релизов.`

`Подсказка: используйте переменную BUILD_NUMBER.`

`В качестве ответа пришлите скриншоты с настройками проекта и результатами выполнения сборки`

`При необходимости прикрепитe сюда скриншоты
![Название скриншота](ссылка на скриншот)`
