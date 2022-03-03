# Django 2.2 Tutorial 
## Austin Wong-Parker | RedShelf
**This repo serves as a note-taking space for anything learned during ths tutorial - specifically Django / Python-related.**

---
1. Part 1:
    * Check Django Version
        1. python -m django --version
    * Q: What is manage.py ?
        1. manage.py: A command-line utility that lets you interact with this Django project in various ways.
    * Q: How to run your Django project?
        1. python manage.py runserver 8080
    * Q: What is URLconf?
        1. A URLconf is like a table of contents for your Django-powered Web site. Basically, it’s a mapping between URLs and the view functions that should be called for those URLs. - Django Book
    * Q: Route?
        1. an argument in path() function that's required. It is a string that contains a URL pattern
    * Q: View?
        1. Once a matching pattern is found, it will call a specific view with a HttpRequest Object as the first argument and any "captured" values from the route as keyword arguments. 
    * Q: kwargs (optional)
        1. Arbitrary keyword arguments can be passed in a dictionary to the target view.
    * Q: name 
        1. Naming specific URLs - allows you to make changes globally and within one file.
2. Part 2:
    * Q: What is migrate doing?
        1. It looks at your INSTALLED_APPS, which is in your settings.py file, and creates any db tables from that settings file. 
    * Q: What are models?
        1. It's your database layout with additional metadata. It contains all the essential fields and behaviors of the data you're storing. Django follows DRY principle. Migrations are derived from your models file.
    * Q: What is a field?
        1. A field in Django are ways for the data types to store a particular type of data. For example: integers would use IntegerField (built-in to Django)
        2. Some field classes will have required arguments such as CharField requires a max_length arg. It uses it for database schema & validation
    * Q: What is a Foreign Key?
        1. Column or group of columns in a relational database table that provides a link between data in two tables - Techopedia
    * Q: What is a Primary Key?
        1. A primary key is a special relational database table column (or combination of columns) designated to uniquely identify each table record. - Techopedia
    * Q: How to tell Django I made changes to my models / made new models?
        1. python manage.py makemigrations polls
    * Q: Soo, what do migrations do again?
        1. Migrations are how Django stores changes to your models (and thus your database schema). They're just files on disk.
        2. the 'migrate' command automatically runs the migrations and manages your database schemas
    * Q: Three step guide to making model changes?
        1. Change your models (**in models.py**)
        2. Run python manage.py makemigrations to create migrations for those changes
        3. Run python manage.py migrate to apply those changes to the database.
    * Q: I have more questions about manage.py? 
        1. [Django Docs for django-admin and manage.py](https://docs.djangoproject.com/en/2.2/ref/django-admin/)
    * Q: Invoke Python shell?
        1. python manage.py shell
        2. FYI - we use this instead of just typing 'python' because manage.py sets DJANGO_SETTINGS_MODULE env variable. This allows Django to import the Python path directly to mysite/settings.py file
    * Q: Why add __str__() to our methods to your models?
        1. Object' representations are automatically-generated throughout Django
    * Q: For tutorial purposes, User/Pass?
        1. admin / redshelf
3. Part 3:
    * Q:
        1.