# Lamp Stack Setup using Docker

First, you have to install [Docker](https://docs.docker.com/engine/install/), of course.

Now, clone this project using ```git clone```:

``` bash
git clone https://github.com/sami-daniel/lamp_stack_docker.git
```

Then you can just enter in the project folder and run it along with docker compose plugin.

``` bash
mv lamp_stack_docker lamp_stack
cd lamp_stack
docker compose up -d
```

The binds are the following, by default. Of course you can, and I recommend you, to alter 
the default configs. 

MYSQL Port -> 3306
PHPMyAdmin -> 8000
Apache Server -> 80 (So you can simple acess it through browser just typing localhost)

The MySql root user does not have any password. So you have to setup one in MySql.

Insinde the project folder, you have a folder called www. Apache by default will use this bind mount
to redirect files to /var/www/html inside the container. So is there you can put your project files, 
and the apache will be capable to serve them.
