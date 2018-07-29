# Docker development environment for Symfony 4.1 app

This is an attempt to create a basic development environment based on 
multiple Docker containers to work on a Symfony 4.1 application.

Disclaimer: this repository is WIP and its content should not be considered production ready code!

# Overview

This development environment provides three different containers:
- Apache
- PHP-FPM
- MariaDB

Apache and PHP-FPM shares a volume containing your application source code while MariaDB stores its
data in a named volume that is persisted across multiple ups and downs.

Custom configuration was kept to a minimum to ensure everybody could easily spin up this environment
and apply only the needed changes without too much bloat.

The Symfony application is simply the basic Symfony 4.1 skeleton with a couple very common bundles 
(ORM and Monolog) that were added to speed up development.  

# Pre-requisites

This repository uses `docker-compose` to run and link multiple containers together. In order to
obtain `docker-compose` you must install it through your OS package manager. If you use Windows
I strongly encourage you to install [Docker Toolbox](https://docs.docker.com/toolbox/overview/).

# Configuration

The application comes with a `.env.dist` file that you can use as a starting point to create 
your `.env` file. The file is used to store both Symfony and Docker environment variables in one place.

# Usage

To start the development environment run:

```
docker-compose up -d
```

You should then be able to access the application at [http://localhost](http://localhost).

To stop it run:

```
docker-compose down
```

# Author

This repository is brought to you by [Stefano Angaran](https://github.com/oniric85).

# Contribution

If you want to contribute just fork this repository, make your changes and create a Pull Request.

Simple. As. That.