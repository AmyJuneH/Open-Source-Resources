# Setting up local for CORE contribution

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
git clone -b 8.8.x https://github.com/drupal/drupal.git d8core
cd d8core
fin config generate
```

   3. Follow the prompts
      * From where should we get your app's codebase? `current working directory`
      * Where is your webroot relative to the init destination? `.`
      * What do you want to call this app? `d8core`
   4. Enter the next commands

```
fin start
fin composer install
```

[docksal] info (shows db creds amongst other things)

## FOR NEW DB

 * DB_HOST=database
 * DB_USER=drupal8
 * DB_PASSWORD=drupal8
 * DB_NAME=drupal8
 * DB_PORT=3306
 
```
    "creds": {
      "user": "user",
      "password": "user",
      "database": "default"
    },
    "internal_connection": {
      "host": "db",
      "port": 3306
 ```
      

## TROUBLESHOOTING


