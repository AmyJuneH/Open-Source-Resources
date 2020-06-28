# Setting up local for CORE contribution

## Assumptions

 * Lando is already intalled and up to date on the machine
 * Git is installed
 * You have basic knowledge of the command line

## Commands

The following set up command will download a Drupal 8 core repeository, start LANDO, and run composer.

   1. Open your terminal of choice.
   2. Enter the following commands
    
```
cd ~
cd Sites/
git clone -b 8.9.x https://github.com/drupal/drupal.git d8core
cd d8core
lando init --recipe drupal8
```

   3. Follow the prompts
      * From where should we get your app's codebase? `current working directory`
      * Where is your webroot relative to the init destination? `.`
      * What do you want to call this app? `d8core`
   4. Enter the next commands

```
lando start
lando composer install
```

`lando info` (shows db creds amongst other things)

## FOR NEW DB

 * DB_HOST=database
 * DB_USER=drupal8
 * DB_PASSWORD=drupal8
 * DB_NAME=drupal8
 * DB_PORT=3306
 
```
    "creds": {
      "user": "drupal8",
      "password": "drupal8",
      "database": "drupal8"
    },
    "internal_connection": {
      "host": "database",
      "port": 3306
 ```
      

## TROUBLESHOOTING

If during the install process after entering your credentials, the website returns that you an existing site, navigate into the file structure:
d8core > sites > default and delete the settings.php file.

```
rm sites/default/settings.php
```

https://docs.devwithlando.io/troubleshooting/logs.html

## RESOURCES

Video: 
From Tandem
https://www.youtube.com/watch?v=jNAdsqQM3RA&feature=youtu.be
