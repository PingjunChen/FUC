django 2
========

Create project
--------

:code:`$ django-admin startproject <project_name>`

Add app
--------

:code:`$ python manage.py startapp <app_name>`


Start server
--------

start server with default port 8000

:code:`$ python manage.py runserver`

start server with specific port num

:code:`$ python manage.py runserver <port_num>`


Create migrations
--------

:code:`$ python manage.py makemigrations`


Migrate database
--------

:code:`$ python manage.py migrate`

Create super user for admin
--------

:code:`$ python manage.py createsuperuser`


Collect static files
--------

:code:`$ python manage.py collectstatic`
