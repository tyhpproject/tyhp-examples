# Expenses

A file-backed command-line expense tracker. Expenses are stored as JSON (the `EXPENSES_FILE` environment variable, or `expenses.json` in the current directory).

Tyhp features in this example: classes, a backed enum, structs, `tyhp/decimal` operators (`+=`, `<=`), `->format()` for totals, and `jsonTryDecodeAs<T>()` to load JSON into a struct. Amounts are stored as decimal strings and converted with `\Tyhp\decimal()` when they are read.

## Install and run

From this directory, with [Tyhp](https://tyhplang.com) and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php help
php build/src/index.php add Cafe food 12.50 lunch
php build/src/index.php add Transit travel 4.25
php build/src/index.php list
php build/src/index.php total
php build/src/index.php remove 1
```

`composer update` installs `tyhp/core`, `tyhp/decimal`, and the other runtime packages `tyhp init` records. `tyhp build` type-checks `src/` and writes PHP under `build/`.

## Commands

| Command | Effect |
| --- | --- |
| `add <payee> <category> <amount> [note]` | Add an expense. The amount is a positive decimal string such as `12.50`. Extra words are the note. |
| `list` | Print id, payee, category, amount, and note, then the total. |
| `total` | Print the total. |
| `remove <id>` | Delete an expense. |

Categories: `food`, `travel`, `supplies`, `other`.
