1. Create an empty dirc and name it your project.
2. sudo pip3 install virtualenv  (if virtualenv is not installed)
3. Create virtual env by 
    **virtualenv venv --python=python3**
4. Activate the virtual env **source venv/bin/activate** 
5. pip install django 
6. pip install djangorestframework 
7. pip install psycopg2-binary
8. django-admin startproject api_template
9. Rename api_template (inner one) to config ( refactor in pycharm else follow the steps below)
    a. Make changes to os.environ.setdefault('DJANGO_SETTINGS_MODULE', 'config.settings') in wsgi.py
    b. os.environ.setdefault('DJANGO_SETTINGS_MODULE', 'config.settings') in asgi.py file
    c. ROOT_URLCONF = 'sampleproject.urls' rename to 'config.urls' in setting.py
    d. os.environ.setdefault('DJANGO_SETTINGS_MODULE', 'config.settings') in manage.py
10. python manage.py makemigrations 
11. python manage.py migrate
12. python manage.py runserver 4000  --- server should be up and running
13. python manage.py startapp app
14. add 'app' in INSTALLED_APPS in setting



