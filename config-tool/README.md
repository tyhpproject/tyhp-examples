# Config check

Loads a dotenv file with `vlucas/phpdotenv` and prints the values, or checks that named keys are set.

Tyhp features in this example: classes, nullable strings, and calling a Packagist PHP library through its `tyhpdef` package.

## Install and run

From this directory, with Tyhp and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php show sample.env
php build/src/index.php check sample.env APP_NAME APP_ENV
```

`check` exits with status 1 when a key is missing or empty. `sample.env` is a stand-in you can copy.

`tyhp.json` lists the generated stubs this project needs under `vendor-tyhpdef/`. The generated PHP 8.0 polyfill stub is omitted because it repeats PHP's `Attribute` class.

## Commands

| Command | Effect |
| --- | --- |
| `show <file.env>` | Print each loaded key. |
| `check <file.env> <KEY> [KEY...]` | Report keys that are missing or empty. |
