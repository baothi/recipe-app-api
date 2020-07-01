# recipe-app-api
Recipe app api source code.
docker build .
docker-compose build
docker-compose run app sh -c "django-admin.py startproject app ."
Setup docker and Django project
sudo chown -R baothi:www-data /home/baothi/recipe-app-api/app

docker-compose run app sh -c "python manage.py test" run ok
docker-compose run app sh -c "python manage.py test && flake8" fail, because build falke8 not yet 
so run: docker-compose build

docker-compose run app sh -c "python manage.py startapp core" ====> create app core

docker-compose run app sh -c "python manage.py test"

docker-compose run app sh -c "python manage.py makemigrations core"  ==> create model

docker-compose run app sh -c "python manage.py test && flake8" 