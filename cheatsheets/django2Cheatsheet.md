# Django2 Cheat Sheet

[Django](https://www.djangoproject.com/) is a high-level Python Web framework that encourages rapid development and clean, pragmatic design.

### Create project
```
$ django-admin startproject <project_name>
```

### Add app
```
$ python manage.py startapp <app_name>
```

### Start server
start server with default port 8000
```
$ python manage.py runserver
```

start server with specific port num
```
$ python manage.py runserver <port_num>
```

### Create migrations
```
$ python manage.py makemigrations
```

### Migrate database
```
$ python manage.py migrate
```

### Create super user for admin
```
$ python manage.py createsuperuser
```

### Collect static files
```
$ python manage.py collectstatic
```
