# Dockerizing a Flask app with Postgres, Nginx & Gunicorn
# Like to learn more?
This [blog post](https://testdriven.io/blog/dockerizing-flask-with-postgres-gunicorn-and-nginx/#media-files) was an excellent resource.
You could also clone this related [github repo](https://github.com/testdrivenio/flask-on-docker)

## How to use this project
### Development
Uses the Flask's built-in WSGI server
Follow these steps after downloading or cloning the repo:
1. Open the project root directory in terminal
2. Run the following command to build the images and run the containers
    $ docker-compose up -d --build
3. Navigate to http://localhost:4000 in your browser. Since the web folder is mounted into the container, your code changes will apply immediately.

### Production
Uses Gunicorn (a production grade WSGI server) and Nginx (a reverse proxy server)
1. Open the project root directory in terminal
2. Run the following command to build the images and run the containers
    $ docker-compose -f docker-compose.prod.yml up -d --build
3. Navigate to http://localhost:1337 in your browser.Since this is a production ready application, no folders are mounted and changes made are only reflected when the image is rebuilt.
