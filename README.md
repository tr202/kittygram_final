# Kittygram

Kittygram социальная сеть владельцев домашних котиков.
## Возможности
- Публикация и  редактирование профиля питомца
- Размещение фото и достижений котика.

## Технологии
- React
- Django
- DRF

## Infra
- Nginx
- Gunicorn
- Docker
- Docker-compose

## CI/CD
- Github Actions

## Production
Kostya https://github.com/tr202

## Запуск проекта
- создайте в домашней директории новую папку
- скопируйте в неё файл docker-compose.production.yml
- сoздайте в этой папке файл .env образец файла .env.example
- выполните следующие команды находясь в новой папке
- sudo docker compose -f docker-compose.production.yml up -d
- sudo docker compose -f docker-compose.production.yml exec backend python manage.py migrate
- sudo docker compose -f docker-compose.production.yml exec backend python manage.py collectstatic
- sudo docker compose -f docker-compose.production.yml exec backend cp -r /app/collected_static/. /backend_static/static/

### Проект будет доступен на ip вашего хоста порт 9000
