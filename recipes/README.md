# Recipe box

A JSON recipe box (`RECIPES_FILE`, or `recipes.json`). `scale` reprints ingredient quantities for a different serving count and leaves the saved recipe unchanged.

Tyhp features in this example: classes, a backed enum, nested structs, `decimal` amounts from `tyhp/decimal`, and `jsonTryDecodeAs<T>()`.

## Install and run

From this directory, with Tyhp and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php add 4 dinner "Weeknight chili"
php build/src/index.php ingredient 1 2 cup broth
php build/src/index.php show 1
php build/src/index.php scale 1 2
```

`tyhp/decimal` is required by the project Composer file (the `tyhp init` post-autoload script adds it).

## Commands

| Command | Effect |
| --- | --- |
| `add <servings> <course> <title>` | Create a recipe. Course is `breakfast`, `lunch`, `dinner`, or `snack`. |
| `ingredient <id> <quantity> <unit> <name>` | Append an ingredient. Quantity is a decimal number. |
| `list` | Print id, course, servings, and title. |
| `show <id>` | Print the saved recipe. |
| `scale <id> <servings>` | Print quantities scaled to another serving count. |
