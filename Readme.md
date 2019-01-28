This is simple Python web application running on Docker Compose. The application uses the Flask framework and maintains a hit counter in Redis.

Build and run:
$ docker-compose up

Open http://localhost:5000 several times.

To stop:
$ docker-compose stop

To rebuild project:
$ docker-compose up --build

Docker file:
 - Build an image starting with the Python 3.4 image.
 - Add the current directory . into the path /code in the image.
 - Set the working directory to /code.
 - Install the Python dependencies.
 - Set the default command for the container to python app.py

Compose file:
 - Defines two services, web and redis.
 - Web service uses an image that’s built from the Dockerfile in the current directory.
 - Forwards the exposed port 5000 on the container to port 5000 on the host machine.
 
Commands:
'docker-compose ps' - active images
'docker image ls' - list installed images
'docker inspect' <image-name> - details of image

More infor at:
https://docs.docker.com/compose/reference/

