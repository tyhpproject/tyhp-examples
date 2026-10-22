# Codes

`encode` lowercases text and prefixes `code:`. The work is done by `Encoder`, which is marked `internal`, and called from `CodeBook` in the same project.

## Install and run

From this directory, with Tyhp and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php help
php build/src/index.php encode Hello
```

## Commands

| Command | Effect |
| --- | --- |
| `encode <text>` | Print `code:` plus the lower-case text. Extra words stay in the text. |
