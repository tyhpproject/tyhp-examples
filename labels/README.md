# Labels

`Note` uses the `Labeled` trait. That trait can only be used by a class that extends `Record` and implements `Titled`, so `label()` can call `getId()` and `getTitle()`.

## Install and run

From this directory, with Tyhp and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php help
php build/src/index.php label 3 Coffee
```

## Commands

| Command | Effect |
| --- | --- |
| `label <id> <title>` | Print `#<id> <title>`. Extra words are part of the title. |
