# django-rest-framework-settings

# install
    pip3 install djangorestframework

        or 

    git clone https://github.com/encode/django-rest-framework


# setting file
        # add rest_framework

        INSTALLED_APPS = [
            'django.contrib.admin',
            'django.contrib.auth',
            'django.contrib.contenttypes',
            'django.contrib.sessions',
            'django.contrib.messages',
            'django.contrib.staticfiles',
            
            'rest_framework',
        ]

        REST_FRAMEWORK = {
            'DEFAULT_PERMISSION_CLASSES': [
                'rest_framework.permissions.DjangoModelPermissionsOrAnonReadOnly'
            ]
        }
# urls file

    # from django.urls import path
    from django.urls import path, include

    path('api-auth/', include('rest_framework.urls'))


# now 
    python3 manage.py migrate
    python3 manage.py runserver

http://127.0.0.1:8000/api-auth/login/
