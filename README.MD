Clair
-----

This is a gcavalcante8808/clair docker image based on clair main image but with support for env variables.

How to see it In Action
-----------------------

You can use ([docker-compose](https://docs.docker.com/compose/install/)) to spin up a PostgreSQL and Clair Servers using the docker-compose.yml file provided in this project in the following way:

```
mkdir test && cd test
wget https://raw.githubusercontent.com/gcavalcante8808/docker-clair/master/docker-compose.yml
docker-compose up
```

The clair container will start and download the latest security entries for debian, ubuntu, rhel and centos.


Needed Environment Variables
----------------------------

The container uses the following environment variables (theh bold ones are **required**) :

 * **DB_HOST**: the IP or hostname of the postgresql Server;
 * DB_USER: a user. If not provided, assumes clair;
 * DB_NAME: the name of the db that will be used. Same value as DB_USER if not provided;
 * **DB_PASSWORD**: the password for the user. If not provided, assumes clair.

ROADMAP
-------

The Following features mark the roadmap for a more usefull (Aka 1.0) version:

 * Support for no-tls config based on env variable.

Author
------

Author: Gabriel Abdalla Cavalcante Silva (gabriel.cavalcante88@gmail.com)

