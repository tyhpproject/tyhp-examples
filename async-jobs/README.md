# Async jobs

Greets one or more names. Each greeting is an `async` method that awaits `Promise::delay()`. The command starts every greeting first, then waits with `Promise::all()`, so the delays overlap.

## Install and run

From this directory, with Tyhp and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php help
php build/src/index.php greet Ada Bob
```

## Commands

| Command | Effect |
| --- | --- |
| `greet <name>...` | Print each name on its own line. The names stay in the order you passed them. |
