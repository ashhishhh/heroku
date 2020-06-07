Drupal on Heroku

System Requirement:
1. Composer
2. Heroku account
3. Terminal or Command prompt

Installation

1. composer create-project --no-install drupal/recommended-project <FolderName>

//Todo
2. Procfile 
2. heroku create
3. git push heroku master
4. heroku ps:scale web=1
5. heroku open
6. Run Drupal installation.
7. Manually create settings.php
    Paste DB configuration.
8. create config/sync folder.
    Create dummy file inside this folder, so that git allows you to commit this directory.    
 

Drush
1. heroku run bash
2. Run drush
    heroku run vendor/bin/drush cr

Redis
1. composer require predis/predis
2. Changes in settings.php

PHP version
Heroku’s PHP support extends to applications using PHP 7.2 (64-bit), PHP 7.3 (64-bit) or PHP 7.4 (64-bit).
To select PHP version 
composer require 'php:~7.2.0'

If your machine/laptop has different version of php running.
You may get following error:
--------------
    Your requirements could not be resolved to an installable set of packages.

    Problem 1
        - This package requires php ~7.3.0 but your PHP version (7.2.21) does not satisfy that requirement.
--------------
To fix this:
composer config platform.php 7.2.0

To Do
2. Xdebug
3. —————
NOTICE: No runtime required in composer.json; requirements
remote:        from dependencies in composer.lock will be used for selection
remote:        - php (7.4.6)
remote:        - ext-gd (bundled with php)
remote:        - ext-mbstring (bundled with php)
remote:        - apache (2.4.43)
remote:        - nginx (1.18.0)
4. https://devcenter.heroku.com/articles/pipelines#github-sync

5. How to modify code, without relaunching the application.

Files folder with write permission

Check free option for image files to retain.