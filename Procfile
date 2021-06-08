release: python manage.py migrate
web: daphne chat_channels.asgi:application --port $PORT --bind 0.0.0.0 -v2
worker: python manage.py runworker channels --settings=chat_channels.settings -v2