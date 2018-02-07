
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
