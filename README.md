ДЗ logging-1
1. Создана ветка logging-1
2. Подготавливаем окружение, обновляем reddit, собираем и пушим образы в dockerhub
3. Устанавливаем язык Go, настраиваем драйвер для работы с Yandex.Cloud
4. Создаем ВМ в Yandex.Cloud
5. Создаем docker-compose-logging.yml для системы логгирования
6. Создаем Dockerfile, fluent.conf для Fluentd и собираем Docker образ
7. Подключаемся к ВМ и запускаем контейнеры и наблюдаем как пишутся логи
8. добавляем драйвер fluentd для сервиса post
9. запускаем контейнер логирования и перезапускаем остальные контейнеры
10. Делаем тестовые посты
11. Заходим на Kibana и наблюдаем логи.
12. Добавляем фильтры во fluentd для service.post
13. добавляем драйвер fluentd для сервиса ui и перезапускаем сервис ui
14. Добавляем фильтры во fluentd для service.ui и перезапускаем сервис fluentd
15. заменяем шаблоны с регулярными выражениями на grok-шаблоны, сначала с одним потом с несколькими
16. Распределенный трейсинг. Добавляем сервис  Zipkin в docker-compose-logging.yml.
17. Включаем его в docker-compose.yml.
18. Переподнимаем инфраструктуру.
19. Заходим на web-интерфейс Zipkin на порту 9411, смотрим и тд.

ДЗ monitoring-1
ссылка на dockerhub https://hub.docker.com/bobastik1982

ДЗ gitlab-ci-1
1. создание ВМ с заданными параметрами с помощью packer
2. установка Docker на ВМб с помощью docker-machine
3. подготовка к развертыванию gitlab на ВМ
    - директории /srv/gitlab/config /srv/gitlab/data /srv/gitlab/logs
    - файл docker-compose.yml
4. развертывание контейнера gitlab на ВМ с помощью docker-compose
5. смена пароль root, отключение регистрации, создание группы, создание проекта, push в gitlab
6. создание pipeline для gitlab (.gitlab-ci.yml)
7. добавление, регистрация и проверка runner
8. добавление reddit в проект gitlab
9. добавление тестов в pipeline
10. добавление окружений dev, stage и production
11. добавление условий (в нашем случае тэг)
12. тестирование динамических окружений.

ДЗ docker-3
1. подключаемся к ранее созданному инстансу на yandex cloud
2. скачиваем папку с шаблонами
3. собираем образы post-py, comment, ui
4. создаем bridge-сеть "reddit" для контейнеров
5. запускаем собранные образы post-py, comment, ui  и проверяем "постим что-ить"
6. cоздаем bridge-сеть "hw-reddit", удаляем и перезапускаем все контейнеры. Проверяем что все работает.
7. останавливаем контейнеры, проверяем размер образов
8. пересобираем образ ui с помощью исходника ubuntu и проверяем что образ 2.0 меньше первого.
9. останавливаем и заново запускаем образы. видим что наши "посты ичезли"
10. создаем  раздел
11. останавливаем и заново запускаем образы с указанием reddit_db:/data/db
12. постим и снова перезапускаем образы: проверяем что посты остались


ДЗ docker-2
1. Создание ветки
2. установка docker? docker-machine, docker-compose
3. Запуск image 'hello world'
4. запуск docker с командами run/start/attach/exec/commit/kill/stop/system df/rm/rmi
5. установка yc
6. Создание instance с помощью yc
7. Деплой docker на удаленном instance с помощью docker-machine
8. Создание docker-контейнера используя Dockerfile, mongod.conf, db_config, start.sh
9. загрузка полчившегося образа на docker hub.
10. развертывание орбраза из docker hub на локальном хосте.
