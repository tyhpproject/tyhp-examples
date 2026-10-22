# Filters

Builds expression trees from inline `fn` predicates on a `Person`, and prints a `PropertyPath` for a field. `adults` prints `age >=`. `city Oslo` prints `city ===`. `column city` prints `city`.

## Install and run

From this directory, with Tyhp and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php help
php build/src/index.php adults
php build/src/index.php city Oslo
php build/src/index.php column city
```

## Commands

| Command | Effect |
| --- | --- |
| `adults` | Print `age >=` from the predicate `age >= 18`. |
| `city <name>` | Print `city ===` from the city predicate. The name is captured in the tree. |
| `column <name\|age\|city>` | Print the property path, such as `city`. |
