# Symbols

Prints values produced by `nameof()`, `default()`, `typeof()`, and `variable_exists()`.

`show` prints:

```text
Reading
label
MAX
text
0
[]
int
reading yes
```

## Install and run

From this directory, with Tyhp and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php help
php build/src/index.php show
```

## Commands

| Command | Effect |
| --- | --- |
| `show` | Print the symbol names, the default `int` and `string`, the type `int`, and whether `$reading` exists. |
