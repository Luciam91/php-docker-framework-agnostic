# Framework Agnostic PHP Development Environment
Got an application that doesn't use a framework? Then here's an easy way to get yourself set up with Docker containers and give yourself an easy development environment!

## Prerequisites
You'll need to ensure you've got Docker installed, just follow the official instructions and you should be good.

[Install Instructions](https://docs.docker.com/engine/installation/)

## Running Your Code
To start your containers simply run

```shell
docker-compose up
```

The compose file provided mounts all of your code to /var/www/html and runs Apache on port 10000. To access your web application just visit `http://localhost:10000` in your favourite web browser.

As well as running your code, this compose configuration launches a MySQL container too. You can access this container from your code on `mysql://database:3306`. If you'd like to connect to the MySQL container from your machine, please use the exposed port instead, `mysql://localhost:10001`.

## Users on OSX
If you're on OSX, or simply using `docker-machine`, you must replace all the `localhost`'s above with the IP address of your `docker-machine`: `docker-machine ip <machine name>`

If you're concerned about the default file-syncing provided by `docker-machine` through VBoxFs, then we recommend disabling it with the flag `--vbox-no-share` and syncing your source code through `rsync` with [docker-machine-rsync](http://github.com/rawkode/docker-machine-rsync)
