Описание проекта "API для Yatube"

Yatube - проект социальной сети. «API для Yatube» расширяет возможности социальной сети. Новый функционал позволяет пользователям публиковать свои посты и управлять подписками через программный интерфейс взаимодействия.
Технологии

    Python - язык программирования.
    Django - свободный фреймворк для веб-приложений на языке Python.
    Django REST Framework - мощный и гибкий набор инструментов для создания веб-API.
    Simple JWT - плагин аутентификации JSON Web Token для Django REST Framework.

Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

git clone https://github.com/greysn/api_final_yatube.git
cd api_final_yatube

Создать и активировать виртуальное окружение:

    python -m venv env
    source venv/Scripts/activate
    python -m pip install --upgrade pip

Установить зависимости из файла requirements.txt: pip install -r requirements.txt Выполнить миграции:

python manage.py makemigrations
python manage.py migrate

После этого, когда все будет установлено, запустите сервер командой: python manage.py runserver

После запуска проекта, документация будет доступна по адресу: [http://localhost:port/redoc/] [Gulp]
Примеры запросов к API:

    Получить публикацию по id (где id=1):

GET /api/v1/posts/1/

    Добавление новой публикации ("text" - обязательное поле): *анонимные запросы запрещены

POST /api/v1/posts
{
  "text": "string",
  "image": "string",
  "group": 0
}

    Работа с группами получение списка доступных сообществ::

 GET /api/v1/groups/