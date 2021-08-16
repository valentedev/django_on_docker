Criar projeto Django
$ docker-compose run django django-admin startproject djangoondocker .

Alterar settings.py
DATABASES = {
'default': {
'ENGINE': 'django.db.backends.postgresql',
'NAME': 'postgres',
'USER': 'postgres',
'PASSWORD': 'postgres',
'HOST': 'db',
'PORT': 5432,
}
}

Migrar banco de dados
$ docker-compose exec django python manage.py migrate

Criar Super User
$ docker-compose exec django python manage.py createsuperuser
