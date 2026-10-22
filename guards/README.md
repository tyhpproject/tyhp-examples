# Guards

`isPositiveInt` is a type guard: its return type is `$value is int`, and the body also requires the int to be greater than zero. After a successful check, the value is an `int`.

## Install and run

From this directory, with Tyhp and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php help
php build/src/index.php check 5
php build/src/index.php check 0
php build/src/index.php check -3
php build/src/index.php check hi
```

## Commands

| Command | Effect |
| --- | --- |
| `check <value>` | `5` prints `positive 5`. `0` and `-3` print `not positive`. Other text prints `not an int`. |
