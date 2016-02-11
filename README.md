# Framework Agnostic PHP Development Environment
Got an application that doesn't use a framework? Then here's an easy way to get yourself set up with Docker containers and give yourself an easy development environment!


### Prerequisites
You'll need to ensure you've got Docker installed, just follow the official instructions and you should be good.

[Install Instructions](https://docs.docker.com/engine/installation/)

### Users on OSX
If you're on OSX you need to sync your code to a VM using docker-machine.

[Rawkode has provided his rsync script that anyone can use](https://github.com/rawkode/docker-machine-rsync)

The compose file provided mounts all of your code to /var/www/html and runs Apache on port 10000, to access your web application just visit http://localhost:10000 in your favourite web browser.

To start your containers simply run
```shell
docker-compose up
```

A MySQL database is provided as well, if you need to connect to this from your code, just reference the container name as your host.
