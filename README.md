# Kitchen

Kitchen is a Dashboard where you can visualize and browse your servers.
It never has been so easy to find and orginize all your nodes!

## How it works

Data is taken from a Chef repository's node data bag

## Installation

We will need:

* sqlite (or another celery broker)
* python 2.6+
* Django 1.3+
* django-celery
* django-kombu *or* RabbitMQ
* Logbook
* Littlechef
* graphviz
* pydot 1.0.25+ (for graphviz graphs)

`apt-get install sqlite3 graphviz`

`pip install django django-celery django-kombu logbook pydot`

`pip install littlechef`

Then create the necessary celery tables

`python manage.py syncdb`

## Running the development server and job queue

To see the web interface on localhost:8000:

`python manage.py runserver`

To start the celerybeat job scheduler

`python manage.py celeryd -B -l info`
