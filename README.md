# Приложение QRKot

## Описание проекта

**QRkot** - это API сервиса по сбору средств для финансирования благотворительных проектов. В сервисе реализована возможность регистрации пользователей, добавления благотворительных проектов и пожертвований, которые распределяются по открытым проектам.

Настроено автоматическое создание первого суперпользователя при запуске проекта.

Реализована возможность получить отчет с перечнем профинансированных проектов, отсортированных по времени, потребовавшимся для полного закрытия.

## Ключевые технологии и библиотеки:
- [Python](https://www.python.org/);
- [FastAPI](https://fastapi.tiangolo.com/);
- [SQLAlchemy](https://pypi.org/project/SQLAlchemy/);
- [Alembic](https://pypi.org/project/alembic/);
- [Pydantic](https://pypi.org/project/pydantic/);
- [Asyncio](https://docs.python.org/3/library/asyncio.html);

## Установка
1. Склонируйте репозиторий:
```
git clone git@github.com:Esposus/cat_charity_fund.git
```
2. Cоздайте и активируйте виртуальное окружение:

```
python -m venv venv
```

* Если у вас Linux/macOS

    ```
    source venv/bin/activate
    ```

* Если у вас windows

    ```
    source venv/scripts/activate
    ```

```
python -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

3. Создайте в корневой директории файл .env со следующим наполнением:

```
APP_TITLE=Кошачий благотворительный фонд
APP_DESCRIPTION=Сервис для поддержки котиков
DATABASE_URL=sqlite+aiosqlite:///./<название базы данных>.db
SECRET=<секретное слово>
FIRST_SUPERUSER_EMAIL=<email суперюзера>
FIRST_SUPERUSER_PASSWORD=<пароль суперюзера>
```
4. Примените миграции для создания базы данных SQLite:
```
alembic upgrade head
```
5. Запустите проект:

```
uvicorn app.main:app --reload
```
Сервис будет запущен и доступен по следующим адресам:
- http://127.0.0.1:8000 - API
- http://127.0.0.1:8000/docs - автоматически сгенерированная документация Swagger
- http://127.0.0.1:8000/redoc - автоматически сгенерированная документация ReDoc


### Автор проекта:

[Дмитрий Морозов](https://github.com/Esposus "GitHub аккаунт")