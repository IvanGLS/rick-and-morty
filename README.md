# rick-and-morty API
 ### How to run

- Create venv: `python -m venv venv`
- Activate venv
- Install requirements: `pip install -r requirements.txt`
- Run migrations: `python manage.py migrate`
- Run Redis Server: `docker run -p 6379:6379 -it redis/redis-stack:latest`
- Run celery for tasks handling: `celery -A rick_and_morty_api worker -l INFO
`
- Run celery beat for task scheduling: `celery -A rick_and_morty_api beat -l INFO --scheduler django_celery_beat.schedulers:Da
tabaseScheduler
`
- Create schedule(admin panel) for running sync in DB
- Run app: `python manage.py runserver`
