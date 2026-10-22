# Convert

`double` is an overloaded method. An `int` argument returns `int`, and a `float` argument returns `float`. The body is a short method (`fn … =>`). `upper` is a short method as well. `find` is overloaded on `int` and `string`, so an id and an email get different result text.

## Install and run

From this directory, with Tyhp and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php help
php build/src/index.php double 4
php build/src/index.php double 1.5
php build/src/index.php upper hello
php build/src/index.php find 12
php build/src/index.php find ada@example.com
```

## Commands

| Command | Effect |
| --- | --- |
| `double <number>` | Print the number times two. `4` prints `8`. `1.5` prints `3`. |
| `upper <text>` | Print the text in upper case. |
| `find <id-or-email>` | `find 12` prints `id 12`. `find ada@example.com` prints `email ada@example.com`. |
