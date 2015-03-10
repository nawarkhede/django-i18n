# django-i18n
Internationalization demo 

#Run django on multiple langusges

First install GNU-TEXT for windows , remember i18n requires GNU-TEXT version >=0.15 , installer available at http://mlocati.github.io/gettext-iconv-windows/

1.Create a django project 

Check USE_I18N  in settings.py is set to true and add following to settings.py

```
LOCALE_PATHS = (
    os.path.join(BASE_DIR, 'locale'),
)
```


Add 'django.middleware.locale.LocaleMiddleware', to MIDDLEWARE_CLASSES classes	

Modify templates

```
{% load i18n %}
{% trans "Hello" %}
```

Now in project root manually create directory named locale and run following command 

```
django-admin.py makemessages -l en
```
```
django-admin.py makemessages -l hr
```

Lets look in locale directory new folder is created according to language , now go in hi folder and and edit the django.po file there are several po file editors availbale for free download , just download anyone and edit.
And add translated string with respectd to original string.


Now change broswers langauge and load the project.

