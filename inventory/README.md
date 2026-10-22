# Inventory catalog

A file-backed command-line inventory. The catalog is stored as JSON (the `INVENTORY_FILE` environment variable, or `inventory.json` in the current directory). Import a CSV once; later commands read that JSON file.

Tyhp features in this example: classes, structs, `int` quantities, reading CSV with PHP `file()` and `str_getcsv`, and `jsonTryDecodeAs<T>()` to load JSON into a struct.

## Install and run

From this directory, with [Tyhp](https://tyhplang.com) and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php help
php build/src/index.php import catalog.csv
php build/src/index.php list
php build/src/index.php adjust WIDGET-1 -2
php build/src/index.php export stock.csv
```

`composer update` installs `tyhp/core` and the other runtime packages `tyhp init` records. `tyhp build` type-checks `src/` and writes PHP under `build/`.

## Commands

| Command | Effect |
| --- | --- |
| `import <file.csv>` | Read `sku,name,quantity,location` rows into the catalog. A header row is skipped. A quantity that is not an integer is reported, and that row is not imported. |
| `list` | Print sku, quantity, location, and name. |
| `adjust <sku> <delta>` | Add an integer delta to the quantity for that sku. The result cannot be negative. |
| `export <file.csv>` | Write the catalog as CSV. |

`catalog.csv` is a sample catalog you can import. Rows already stored under the same sku are updated. Other skus stay in the JSON file. Import exits with status 1 when any row is reported as an error.
