# Docker: Drupal 8

[Docker](http://docker.com) image aimed for [Drupal](http://drupal.org) 8 development, using [Docker Forge](http://github.com/robloach/forge).

http://github.com/robloach/docker-drupal8


## Features

* [Docker Forge](http://github.com/robloach/forge)
* [Apache](http://apache.org) 2.4.7
* [PHP](http://php.net) 5.5.9
* [MySQL](http://mysql.com) 5.5.37
* [phpMyAdmin](http://phpmyadmin.net) 4.0.10
* [Composer](http://getcomposer.org) 1.0.0-alpha8
* [Drush](http://github.com/drush-ops/drush) master


## Usage

### Install

Pull `robloach/drupal8` from the Docker repository:
```
docker pull robloach/docker-drupal8
```

Or build `robloach/docker-drupal8` from source:
```
git clone https://github.com/RobLoach/docker-drupal8.git
docker build -t robloach/docker-drupal8 robloach/docker-drupal8
```

### Run

Run the image, binding associated ports, and mounting the present working
directory:

```
docker run -p 880:80 -p 222:22 -v $(pwd)/drupal:/var/www/html:rw robloach/docker-drupal8
```


### Work In Progress

This is in no means production, or even development-ready. Contributions are
more than welcome.


## Services

Service     | Port | Usage
------------|------|------
SSH         | 22   | Connect with `ssh root@localhost -p 422` with the password `root`
Apache      | 80   | Visit `http://localhost:880` in your browser
PHPMyAdmin  | 80   | Visit `http://localhost:880/phpmyadmin` in your browser


## Volumes

Volume          | Description
----------------|-------------
`/var/www/html` | The location of the web root.
