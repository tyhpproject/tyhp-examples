# Chirper

The Laravel Chirper bootcamp (https://github.com/laravel/bootcamp and https://laravel.com/learn/getting-started-with-laravel), written in Tyhp.

Chirps are `tyhp/rhetoric` models (`App\Data\Chirp`, `App\Data\Author`, `App\Data\ChirpContext`). `User` stays the Eloquent authenticatable. The two share the `users` table: Rhetoric reads `id`, `name`, and `email` for the chirp author, and Eloquent owns registration and login.

Tyhp in this example: controllers, models, the service provider, the user factory, the database seeder, routes, and tests. Laravel is typed through `tyhpdef/laravel-framework`, `tyhpdef/fakerphp-faker`, and the Illuminate tyhpdef packages.

Laravel loads `config/`, `database/migrations/`, `bootstrap/app.php`, `bootstrap/providers.php`, `public/index.php`, and `artisan` as PHP from those paths. Blade views stay in `resources/views/`. `config/rhetoric.php` registers `ChirpContext`.

`composer.json` requires `tyhp/rhetoric` with the other `tyhp/*` packages. The package provider registers the context from that config.

## Install and run

From this directory, with [Tyhp](https://tyhplang.com) and PHP 8.5 on your PATH:

```bash
composer install
tyhp build
cp .env.example .env
php artisan key:generate
touch database/database.sqlite
php artisan migrate
php artisan serve
```

Open http://127.0.0.1:8000. Register, log in, and post a chirp.

## Tests

```bash
vendor/bin/phpunit
```
