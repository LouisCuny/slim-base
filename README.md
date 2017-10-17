# Slim base - A Slim 3 skeleton (fork)

This is a skeleton for Slim PHP micro-framework to get started quickly

## Features
- Eloquent ORM
- Flash messages
- CSRF protection
- Authentication (Sentinel)
- Validation (Respect)
- Twig templating engine (cache, debug)
- Bootstrap 4
- Helpers for assets management, redirections, ...

## Installation
### 1. Create project using Composer
``` bash
$ composer create-project louis-cuny/slim-base [app-name]
```

### 2. Create database

Create your database and fill `app/parameters.yml`

### 3. Create tables
``` bash
$ php bin/console db 
```

## Key files
- `public/index.php`: Application entry point
- `var/cache/twig/`: Twig cache
- `app/`: Configuration files
    - `controllers.php`: Registers every controller in the app container
    - `database.php`: Script for creating database tables
    - `parameters.yml`: Database configuration file (put your database configuration here)
    - `dependencies.php`: Services for Pimple
    - `handlers.php`: Slim error handlers
    - `middleware.php`: Application middleware
    - `settings.php`: Application configuration
- `src/`
    - `App/`
        - `Controller/`: Application controllers
            - `Controller.php`: Base controller. All controllers should extend this class
        - `Middleware/`: Application middleware
        - `Model/`: Eloquent model classes
        - `Resources/`
            - `routes/`: Application routes
                - `app.php`: Main routing file
                - `auth.php`: Routing file for authentication
            - `views/`: Twig templates
