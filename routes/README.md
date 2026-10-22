# Routes

`widgets` and `orders` return paths whose type is the template `api/${string}/items`.

## Install and run

From this directory, with Tyhp and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php help
php build/src/index.php widgets
php build/src/index.php orders
```

## Commands

| Command | Effect |
| --- | --- |
| `widgets` | Print `api/widgets/items`. |
| `orders` | Print `api/orders/items`. |
