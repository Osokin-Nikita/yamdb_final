# CI/CD для проекта API YAMDB
REST API для сервиса YaMDb — базы отзывов о фильмах, книгах и музыке. 


## Проверка workflow
![Django-app workflow](https://github.com/needred/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)

## Workflow
* tests - Проверка кода на соответствие стандарту PEP8 (с помощью пакета flake8) и запуск pytest. Дальнейшие шаги выполнятся только если push был в ветку master или main.
* build_and_push_to_docker_hub - Сборка и доставка докер-образов на Docker Hub
* deploy - Автоматический деплой проекта на боевой сервер. Выполняется копирование файлов из репозитория на сервер:
* send_message - Отправка уведомления в Telegram. Отправка уведомления происходит только при положительном выполнении инструкций Workflow
