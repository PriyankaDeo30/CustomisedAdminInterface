# CustomisedAdminInterface
This repository contains code for creating a custom administration interface for Django projects using AdminLTE.

#Installation Steps
Follow these steps to set up the project:

#Install Django: If you haven't already installed Django, you can do so using pip:

pip install django

#Create Django Project: Create a new Django project using the following command:
django-admin startproject myproject

#Install AdminLTE: Install AdminLTE and its dependencies using pip:
pip install django-adminlte3 django-adminlte3_theme

#Configure Static Root: In your Django project's settings.py file, include the installed apps 'adminlte3' and 'adminlte3_theme'. Also, configure the STATIC_ROOT to collect static files:

INSTALLED_APPS = [
    ...
    'adminlte3',
    'adminlte3_theme',
    ...
]

STATIC_ROOT = os.path.join(BASE_DIR, 'staticfiles')

#Collect Static Files: Run the collectstatic management command to collect static files into the designated directory:
python manage.py collectstatic

#Run Migrations: Apply database migrations to create necessary database tables:
python manage.py makemigrations
python manage.py migrate

#Run Development Server: Start the Django development server:
python manage.py runserver

Now, you can access your Django project with the customized AdminLTE admin interface by visiting http://127.0.0.1:8000/admin/.
