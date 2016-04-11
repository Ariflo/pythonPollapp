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

##Routes

- set up routes on the url.py page
- URL patterns are regular expressions

Each view is responsible for doing one of two things:<br>

-	Returning an HttpResponse object containing the content for the requested page<br>
-  Raising an exception such as Http404.

##Django Design Principles 
One of the foremost design goals of Django is to maintain loose coupling. Some controlled coupling is introduced in the django.shortcuts module.

##Generic Views System
A common case of basic Web development: getting data from the database according to a parameter passed in the URL, loading a template and returning the rendered template. Because this is so common, Django provides a shortcut, called the “generic views” system.

Generic views abstract common patterns to the point where you don’t even need to write Python code to write an app.