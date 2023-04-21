## Проект: запуск docker-compose
### Docker предоставляет возможность передать приложение «вместе с компьютером». Для управления взаимодействием нескольких контейнеров применяют утилиту docker-compose.

## Используемые технологии:
### Python 3.7
### Django 2.2.16
### djangorestframework 3.12.4
### gunicorn 20.0.4

## Запуск проекта
- Клонировать репозиторий и перейти в него в командной строке:
```git@github.com:DmitryOstrovskiy/infra_sp2.git```
```cd api_yamdb```

- Cоздать и активировать виртуальное окружение:
```python -m venv venv```
```source venv/Scripts/activate```

- Установить зависимости из файла requirements.txt:
```python -m pip install --upgrade pip```
```pip install -r requirements.txt```

- Выполнить миграции:
```python manage.py migrate```

- Запустить проект:
```python manage.py runserver```

## Заполнение базами данных
### копируем файл с базами данных из /infra в папку app

### docker cp fixtures.json <id контенера>:/app
### запускаем команду для загрузки баз

### docker-compose exec web python manage.py loaddata fixtures.json