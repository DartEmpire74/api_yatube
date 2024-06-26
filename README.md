# api_yatube - API для социальной сети Yatube

## Установка

1. Клонируйте репозиторий:

    git clone https://github.com/your-username/api_yatube.git
    cd api_yatube

2. Создайте и активируйте виртуальное окружение: 

    python -m venv venv

3. Установите зависимости:  

    pip install -r requirements.txt

4. Примените миграции: 

    python manage.py migrate

5. Запустите сервер разработки:

    python manage.py runserver
    
По умолчанию, сайт будет доступен по адресу http://127.0.0.1:8000/.


## Аутентификация
    
    В проекте реализована аутентификацию по токену TokenAuthentication.


## Эндпоинты 

    api/v1/api-token-auth/ (POST): передаём логин и пароль, получаем токен.
    api/v1/posts/ (GET, POST): получаем список всех постов или создаём новый пост.
    api/v1/posts/{post_id}/ (GET, PUT, PATCH, DELETE): получаем, редактируем или удаляем пост по id.
    api/v1/groups/ (GET): получаем список всех групп.
    api/v1/groups/{group_id}/ (GET): получаем информацию о группе по id.
    api/v1/posts/{post_id}/comments/ (GET, POST): получаем список всех комментариев поста с id=post_id или создаём новый, указав id поста, который хотим прокомментировать.
    api/v1/posts/{post_id}/comments/{comment_id}/ (GET, PUT, PATCH, DELETE): получаем, редактируем или удаляем комментарий по id у поста с id=post_id.

## Автор проекта

    https://github.com/DartEmpire74
