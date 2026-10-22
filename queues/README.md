# Queues

Pushes command arguments onto `\SplQueue<string>` and prints them back in order. `enqueue` takes a `string`, and `dequeue` returns a `string`, because the queue is a generic PHP class from `tyhpdef/php`.

## Install and run

From this directory, with Tyhp and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php help
php build/src/index.php push alpha beta
```

## Commands

| Command | Effect |
| --- | --- |
| `push <item>...` | Print how many items were queued, then each item. |
