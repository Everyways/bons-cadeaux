# For first time only !
    docker compose up -d --build
    docker compose exec phpmyadmin chmod 777 /sessions
    docker compose exec php bash
    chown -R www-data:www-data /var/www/storage /var/www/bootstrap/cache
    chmod -R 775 /var/www/storage /var/www/bootstrap/cache
    composer install
    php artisan migrate

#From the second time onwards

    docker compose up -d

# Laravel App

    URL: http://localhost

# Mailpit

    URL: http://localhost:8025

# phpMyAdmin

    URL: http://localhost:8080
    Server: db
    Username: 
    Password: 
    Database: 

# Adminer

    URL: http://localhost:9090
    Server: db
    Username: 
    Password: 
    Database: 

# Basic docker compose commands

    Build or rebuild services
        docker compose build
    Create and start containers
        docker compose up -d
    Stop and remove containers, networks
        docker compose down
    Stop all services
        docker compose stop
    Restart service containers
        docker compose restart
    Run a command inside a container
        docker compose exec [container] [command]

# Useful Laravel Commands

    Display basic information about your application
        php artisan about
    Remove the configuration cache file
        php artisan config:clear
    Flush the application cache
        php artisan cache:clear
    Clear all cached events and listeners
        php artisan event:clear
    Delete all of the jobs from the specified queue
        php artisan queue:clear
    Remove the route cache file
        php artisan route:clear
    Clear all compiled view files
        php artisan view:clear
    Remove the compiled class file
        php artisan clear-compiled
    Remove the cached bootstrap files
        php artisan optimize:clear
    Delete the cached mutex files created by scheduler
        php artisan schedule:clear-cache
    Flush expired password reset tokens
        php artisan auth:clear-resets

# Laravel Pint (Code Style Fixer | PHP-CS-Fixer)

    Format all files
        vendor/bin/pint
    Format specific files or directories
        vendor/bin/pint app/Models
        vendor/bin/pint app/Models/User.php
    Format all files with preview
        vendor/bin/pint -v
    Format uncommitted changes according to Git
        vendor/bin/pint --dirty
    Inspect all files
        vendor/bin/pint --test

# Rector

    Dry Run
        vendor/bin/rector process --dry-run
    Process
        vendor/bin/rector process
