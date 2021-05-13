1. cd ~/django-on-docker
2. sudo docker-compose -f docker-compose.prod.yml up -d --build
3. sudo docker-compose -f docker-compose.prod.yml exec web python manage.py migrate --noinput
4. sudo docker-compose -f docker-compose.prod.yml exec web python manage.py collectstatic --no-input --clear