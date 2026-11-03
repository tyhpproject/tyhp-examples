# Routes

`Paths::items()` builds `api/{resource}/items` from a resource name. Its return type is the template
`api/${string}/items`, and the interpolation `"api/{$resource}/items"` matches that pattern.

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
