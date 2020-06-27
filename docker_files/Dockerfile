# Dockerfile
FROM my_django_env
ADD . /app
WORKDIR /app

# EXPOSE port 8000 to allow communication to/from server
EXPOSE 8000
RUN find /app -name '*.pyc' -delete