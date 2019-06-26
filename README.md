Start
$ docker-composer up -d

Open debug console:
$ docker attach app

Open app terminal:
$ docker-composer exec app bash

Create new app:
$ docker-compose run app rails new . --force --no-deps --database=mysql
$ sudo chown -R $USER:$USER .
