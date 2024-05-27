# use the golang:alpine base image
FROM python:3.8

# copy all the files from the current directory to the container working directory
ADD . .

# set the working directory to /go/src/app
WORKDIR /project/techtrends

RUN pip install -r requirements.txt
RUN python init_db.py

# expose the port
EXPOSE 3111

# start the container
CMD ["python", "app.py"]