
## Update 8.3 to 8.4

Updating from 8.3 to 8.4 should be pretty straightforwarded. Anyway, please try
this first in your local dev-environment.

Please check the [CHANGELOG](https://github.com/markaspot/markaspot/blob/8.4.x-dev/CHANGELOG.md) for changes.

```
$ composer update
$ cd web
$ drush sql-dump > /var/www/backups/somewhere.sql
$ drush updatedb
  The following updates are pending:

  markaspot module :
    8001 -   Enables the twig_tweak and markaspot_trend modules.
    8002 -   Update the stats view.
    8003 -   Enable Mark-a-Spot Front module
    8004 -   Enable Mark-a-Spot Request ID module
    8005 -   Move Service Request IDs

  Do you wish to run all pending updates? (y/n): y
  Performing markaspot_update_8001                                                                                             [ok]
  Performing markaspot_update_8002                                                                                             [ok]
  Performing markaspot_update_8003                                                                                             [ok]
  Performing markaspot_update_8004                                                                                             [ok]
  Performing markaspot_update_8005                                                                                             [ok]
  Cache rebuild complete.                                                                                                      [ok]
  Finished performing updates.
```

This command will install the Mark-a-Spot distribution into a project directory, which will be a good starting point.
