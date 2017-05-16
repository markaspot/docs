# Welcome to Mark-a-Spot
*A Drupal 8 distribution*

<img src="img/logo.png" alt="Logo" style="margin: -20px 20px 0 0; float:left; width: 120px;"/>

Mark-a-Spot is a fully responsive mobile and desktop tool for public civic issue reporting and crowdmapping, idea-management, civic engagement with a localization perspective. It's based on [Drupal 8](https://drupal.org).

## About this documentation

We assume you use the Docksal integration that comes along with the project repo. It brings all necessary tools out of the box. All commands and URLs will also work in any local or production environment.

Please help improving it. You can send pull requests anytime. If you find bugs don't hesitate to [file an issue](https://github.com/markaspot/mark-a-spot/issues).

## Installation

The easiest way to run a ready-to-use Mark-a-Spot platform is by installing it via composer. This is how you get the latest code base: 

```
$ curl -s https://getcomposer.org/installer | php
$ sudo mv composer.phar /usr/local/bin/composer
$ composer create-project markaspot/mark-a-spot project-dir --stability dev
```

This command will install the Mark-a-Spot distribution into a project directory, which will be a good starting point.

You may then use the [included](https://github.com/markaspot/mark-a-spot/tree/master/.docksal) Docksal integration for easy development.
If you have drush installed replace the connection string with credentials of your database and run the following drush command. You can also point your browser to a virtual host that refers to `project-dir/web`.


```
$ cd project-dir
$ fin start
$ cd web
$ fin exec drush si markaspot -y  --db-url=mysql://user:user@db:3306/default
```
This can take some minutes. You might being asked for an SSH key passphrase after submitting `fin start` command, see further instructions [here](http://docksal.readthedocs.io/en/master/getting-started/project-setup/). After the installation process you will see 

```
[...] 
Installation complete.  User name: admin  User password: WDjMNSYz7F            

Features bundle Mark-a-Spot automatically created.                                                                                                              [status]
User saved                                                                                                                                                      [status]
Default Open311 page was updated with a new server hostname                                                                                                     [status]
Congratulations, you installed Mark-a-Spot!
```

Copy the password and switch to the browser and start [configuration](configuration.md). 
