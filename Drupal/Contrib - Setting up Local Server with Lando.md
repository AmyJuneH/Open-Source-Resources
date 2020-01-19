# Setting up local for CONTRIB contribution

## Assumptions

 * Lando is already intalled and up to date on the machine
 * Git is installed
 * You have basic knowledge of the command line

## Commands

The following set up command will download a Drupal 8 core repeository, start LANDO, and run composer.

   1. Open your terminal of choice.
   2. Enter the following commands
    
```
composer create-project drupal-composer/drupal-project:8.x-dev d8landosandbox --stability dev --no-interaction
```

   3. cd into site

```
lando init --recipe drupal8
```

   4. Follow the prompts
      * From where should we get your app's codebase? `current working directory`
      * Where is your webroot relative to the init destination? `web`
      * What do you want to call this app? `d-8-sandbox`
   5. Enter the next commands

```
lando start
```

lando info (shows db creds amongst other things)

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

https://docs.devwithlando.io/troubleshooting/logs.html

## RESOURCES

Video: 
From Tandem
Installing Lando
https://docs.devwithlando.io/installation/installing.html

(after Lando is installed)
https://www.youtube.com/watch?v=JGef7Fx44F4&t=4s
