cd ~/django-on-docker
sudo docker-compose -f docker-compose.prod.yml up -d --build
sudo docker-compose -f docker-compose.prod.yml exec web python manage.py migrate --noinput
sudo docker-compose -f docker-compose.prod.yml exec web python manage.py collectstatic --no-input --clear