# Short links

A local registry of short codes and target URLs. Resolving a code prints the URL. The tool does not open a network connection.

Tyhp features in this example: an extension method on `string` (`toSlug()`), structs, classes, and JSON loaded with `jsonTryDecodeAs<T>()`.

## Install and run

From this directory, with Tyhp and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php slug Launch Post
php build/src/index.php add "Launch Post" https://example.com/launch
php build/src/index.php resolve launch-post
php build/src/index.php list
```

Links are stored in `SHORTLINKS_FILE`, or `shortlinks.json` in the current directory.

## Commands

| Command | Effect |
| --- | --- |
| `add <code-or-title> <url>` | Save a link. The code is turned into a slug. The URL must include a scheme. |
| `list` | Print each code and target. |
| `resolve <code>` | Print the target URL. |
| `remove <code>` | Delete a link. |
| `slug <words>` | Print a slug without saving it. |
