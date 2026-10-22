# Vectors

A `Vec` with `+`, `*`, and `==` operator overloads. `add 1 2 3 4` prints `4,6`. `scale 2 3 4` prints `8,12`.

## Install and run

From this directory, with Tyhp and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php help
php build/src/index.php add 1 2 3 4
php build/src/index.php scale 2 3 4
php build/src/index.php eq 1 2 1 2
php build/src/index.php eq 1 2 3 4
```

## Commands

| Command | Effect |
| --- | --- |
| `add <x1> <y1> <x2> <y2>` | Print the sum as `x,y`. |
| `scale <x> <y> <factor>` | Print the scaled vector as `x,y`. |
| `eq <x1> <y1> <x2> <y2>` | Print `yes` when the vectors are equal, otherwise `no`. |
