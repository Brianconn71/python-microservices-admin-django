FROM python:3.9
# Gets the 3.9 version of python for docker image

# to get the logs and see whats happening
ENV PYTHONUNBUFFERED 1

# CREATE THE WORKING DIRECTORY WITHIN THE CONTAINER
WORKDIR /app

# copy the requirements.txt file from the local machine to the container.
COPY requirements.txt /app/requirements.txt

# install the requirements.txt file inside the container
RUN pip install -r requirements.txt

# copy all the files from the local machine folder repo to the container
COPY . /app/

# run the server once the container is created, we also need to specify the coontainer port to run derver on otherise we cant connect on our local machine
CMD python manage.py runserver 0.0.0.0:8080
