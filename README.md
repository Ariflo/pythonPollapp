##How to properly set-up postgresSQL DB with python
```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'polls_db',
        'USER': '',
        'PASSWORD': '',
        'HOST': '127.0.0.1',
        'PORT': '5432',
    }
}
```

##Three-step guide to making model changes:

-	Change your models (in models.py).
-	Run ```python manage.py makemigrations``` to create migrations for those changes
-	Run ```python manage.py migrate``` to apply those changes to the database.