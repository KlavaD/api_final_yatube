## версия API-YATUBE!
### Данная версия готова для слияния с Frontend-ом, чтобы, наконец-то, стать социальной сетью для публикации постов с картинками, комментариями и последователями!
В данном проекте использованы технологии:
Python, Django, DRF, Api

**Как запустить проект:**
Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/KlavaD/api_final_yatube.git
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:
```
python3 -m venv env
```

* Если у вас Linux/macOS
```
source env/bin/activate
```

* Если у вас windows
```
source env/scripts/activate
```

Обновить pip:
```
python3 -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:
```
pip install -r requirements.txt
```

Выполнить миграции:
```
python3 manage.py migrate
```

Запустить проект:
```
python3 manage.py runserver
```

## Примеры запросов: ##
Создание пользователя:
Получение токена:

Получение публикаций:
>**GET** http://127.0.0.1:8000/api/v1/posts/

Создание публикации:
>**POST** http://127.0.0.1:8000/api/v1/posts/
```
{
  "text": "string",
  ...
}
```

Получение списка групп:
>**GET** http://127.0.0.1:8000/api/v1/groups/

Просмотр комментариев к публикации:
>**GET** http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/

Создание комментариев к публикации:
>**POST** http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/
```
{
  "text": "string"
}
```

Посмотреть всех подписчиков пользователя:
>**GET** http://127.0.0.1:8000/api/v1/follow/

Подписаться на автора:
>**POST** http://127.0.0.1:8000/api/v1/follow/
```
{
  "following": "string"(username)
}
```

Документация для API Yatube:
> http://127.0.0.1:8000/redoc/
