# Kittygram
Kittygram - веб-приложение для публикации фотографий котов.  
Пользователи могут регистрироваться, добавлять котов, загружать фотографии и просматривать их через веб-интерфейс и API.

Функциональность
- Регистрация и авторизация пользователей (Djoser + TokenAuth)
- Добавление и редактирование карточек котов
- Загрузка изображений котов
- REST API на Django REST Framework
- Админ-панель Django
- SPA интерфейс на React
- Раздача через Nginx

Стек технологий

Backend:
- Python 3.10
- Django
- Django REST Framework
- Djoser
- PostgreSQL
- Gunicorn

Frontend:
- React
- JavaScript
- HTML/CSS

DevOps:
- Docker
- Docker Compose
- Nginx
- GitHub Actions (CI/CD)

Медиа и статика
Static files обслуживаются через Nginx
Media файлы сохраняются в Docker volume и доступны по /media/

CI/CD

Проект использует GitHub Actions:
Запуск тестов при push
Сборка Docker образов
Отправка образов в DockerHub


Запуск проекта
1) Клонировать репозиторий
git clone repo-url
cd kittygram_final
2) Создать .env файл
POSTGRES_DB=kittygram
POSTGRES_USER=kittygram_user
POSTGRES_PASSWORD=kittygram_password

DB_HOST=db
DB_PORT=5432

SECRET_KEY=your-secret-key
DEBUG=False
ALLOWED_HOSTS=localhost,127.0.0.1

3) docker compose up -d --build

Доступ к сервисам
Frontend: http://localhost
API: http://localhost/api/
Admin: http://localhost/admin/