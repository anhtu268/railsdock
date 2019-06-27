Start
$ docker-compose build
$ docker-compose up -d

Open app terminal:
$ docker attach app

Create new app:
$ rails new . --force --no-deps --database=mysql
$ sudo chown -R $USER:$USER ./*
