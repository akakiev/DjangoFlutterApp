Source: 

    https://medium.com/@clever.tech.memes/django-and-flutter-a-step-by-step-tutorial-for-a-boilerplate-application-f564335f2e8b
    https://github.com/CleverTechMemes/DjangoFlutterBoilerplaceApplication

Instruction to create the template for the project:

1. mkdir backend frontend
2. conda activate django_flutter_env
3. Click on the extensions and install the useful extensions including “Awesome Flutter Snippets”, “Dart”, “Flutter”, “Prettier”, “Python”, “Django”
4. django-admin startproject backendapp .
5. python manage.py startapp backendcore
6. add app to the settings.py
7. python manage.py migrate
8. python manage.py runserver
9. TIME_ZONE = "Europe/Warsaw"
10. create .env file in te same folder as settings.py file, add to .env SECRET_KEY and DEBUG any space between variable and key-value(i.e KEY=my_key)
11. add to the settings.py file:
    env = environ.Env()
    environ.Env.read_env()
    SECRET_KEY = env('SECRET_KEY')
    DEBUG = env('DEBUG')
12. create a Flutter project in VSCODE using “CTRL + SHIFT + P” and selecting “Create Flutter Application”, and then select the folder for creating the flutter application
13. add http dependency to Flutter
    flutter pub add http
14. install Django Rest Framework and add the rest framework to the installed apps
    pip install django-rest-framework
15. install the simple-jwt and the django cors headers. We require simple-jwt, to activate the token authentication in Django and we require cors-origin because we need to communicate with an external frontend like Flutter
    pip install django-cors-headers
    pip install djangorestframework-simplejwt
16. add to the settings.py file rest_framework, crosheaders, allowed hosts
17. VSC -> View -> Command Palette or Ctrl+shift+p and type Python Select Interpreter And select the correct interpreter for my project
18. in the settings.py file add actual flutter url to the CORS_ORIGIN_WHITELIST