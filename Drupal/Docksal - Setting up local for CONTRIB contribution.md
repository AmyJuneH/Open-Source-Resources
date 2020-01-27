# Setting up local for CONTRIB contribution

## Assumptions

 * Docksal is already intalled and up to date on the machine
 * Git is installed
 * You have basic knowledge of the command line

## Commands

The following set up command will download a Drupal 8 core repeository, start [docksal], and run composer.

   1. Open your terminal of choice.
   2. Enter the following commands
    
```
cd ~
cd Sites/
composer create-project drupal-composer/drupal-project:8.x-dev d8landosandbox --stability dev --no-interaction
```

   3. cd into site

```
fin config generate
```

   4. Follow the prompts
      * From where should we get your app's codebase? `current working directory`
      * Where is your webroot relative to the init destination? `web`
      * What do you want to call this app? `d-8-sandbox`
   5. Enter the next command

```
fin start
```

[docksal] info (shows db creds amongst other things)

## FOR NEW DB

 * DB_HOST=db
 * DB_USER=user
 * DB_PASSWORD=user
 * DB_NAME=default
 * DB_PORT=3306
 
```
    "creds": {
      "user": "user",
      "password": "user",
      "database": "db"
    },
    "internal_connection": {
      "host": "db",
      "port": 3306
 ```
      

## TROUBLESHOOTING
