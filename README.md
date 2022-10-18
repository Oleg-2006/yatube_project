#  Yatube

##  Описание
Проект Yatube - это социальная сеть. Она даст пользователям возможность создать учетную запись,
публиковать записи, подписываться на любимых авторов и отмечать понравившиеся записи.

##  Используемые технологии
- Python3
- Django
- SQLite
- Unittest
- HTML

##  Функциональность
В проекте реализованы:
- создание учётной записи администратора и управление сайтом через интерфейс администрирования
- регистрация и авторизация на сайте самостоятельно
- возможность публиковать посты
- подписки на других авторов
- возможность комментировать посты

##  Запуск проекта локально
- Клонировать репозиторий
```
git@github.com:Oleg-2006/yatube_project.git
```
- Перейти в новую директорию
```
cd yatube_project/
```
- Инициализировать виртуальное окружение
```
python -m venv venv
```
- Активировать виртуальное окружение
```
source venv/Scripts/activate
```
- Обновить pip и установить зависимости проекта
```
python -m pip install --upgrade pip
pip install -r requirements.txt
```
- Из каталога с файлом `manage.py` запустить миграции
```
python manage.py migrate
```
- Создать супер-пользователя
```
python manage.py createsuperuser
```
- Соберите статику
```
python manage.py collectstatic
```
- Для отключения режима отладки необходимо изменить в `yatube.settings.py` на
```
DEBUG = False
```
- Запуск проекта
```
python manage.py runserver
```

##  Приложения проекта
Все приложения проекта покрыты тестами.
Чтобы запустить тесты необходимо из директории `yatube/` вызвать
```
python manage.py test -v {0,1,2,3}
```
*где 0- без подробностей, 3 - максимум информации*
### posts
Приложение отвечает за:
- отображение главной страницы
- отображение страницы группы
- отображение страницы пользователя
- отображение страницы поста
- создание поста
- редактирование поста
- создания комментария
- отображения страницы подписок
- добавление подписок
- удаление подписок
- настройки админки
### about
Приложение отвечает за:
- отображение страницы об авторе
- отображение страницы технологии
### users
Приложение отвечает за:
- регистрацию пользователя
- авторизацию
- выход из аккаунта
- сброс и смену пароля
### core
Приложение отвечает за контекст-процессоры:
- отображение текущего года на страницах
- кастомной страницы 404 
- кастомной страницы 403
- кастомной страницы 500
