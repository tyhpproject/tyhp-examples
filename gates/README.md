# Gates

Three small probes:

- `length` chooses `mb_strlen` when the `mbstring` extension is loaded, and `strlen` otherwise. The choice is a `declare(ext=…)` pair.
- `php` prints `8.5` on PHP 8.5 and `8.6+` on later PHP. The two branches are `declare(php=…)`.
- `first` calls `array_first` from a method marked `#[\Tyhp\Php(">=8.5")]`.

## Install and run

From this directory, with Tyhp and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php help
php build/src/index.php length café
php build/src/index.php php
php build/src/index.php first alpha beta
```

On PHP 8.5 with `mbstring`, `length café` prints `mbstring 4`, `php` prints `8.5`, and `first` prints `alpha`.

## Commands

| Command | Effect |
| --- | --- |
| `length <text>` | Print `mbstring` or `bytes`, then the character or byte length. |
| `php` | Print `8.5` or `8.6+`. |
| `first <item>...` | Print the first item. |
