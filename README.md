# recipe-app-api
Recipe app api source code.
docker build .
docker-compose build
docker-compose run app sh -c "django-admin.py startproject app ."
Setup docker and Django project