# Bookmarks

A file-backed command-line bookmark manager. Each bookmark has a title, a URL, comma-separated tags, and an optional note. Bookmarks are stored as JSON (the `BOOKMARKS_FILE` environment variable, or `bookmarks.json` in the current directory).

Tyhp features in this example: classes, a backed enum (`Command`), a literal union (`SearchScope`), structs, a nullable `note` field, string methods from `tyhp/core` (`trim`, `isEmpty`, `toLower`, `contains`), and `jsonTryDecodeAs<T>()` to load JSON into a struct.

## Install and run

From this directory, with [Tyhp](https://tyhplang.com) and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php help
php build/src/index.php add "Tyhp docs" https://tyhplang.com docs,tyhp "language site"
php build/src/index.php list
php build/src/index.php search tyhp
php build/src/index.php remove 1
```

`composer update` installs `tyhp/core` and the other runtime packages `tyhp init` records. `tyhp build` type-checks `src/` and writes PHP under `build/`.

## Commands

| Command | Effect |
| --- | --- |
| `add <title> <url> <tags> [note]` | Save a bookmark. Tags are comma-separated. Quote a title that contains spaces. The URL must include a scheme, such as `https://`. |
| `list` | Print id, title, URL, tags, and note. |
| `search [--title\|--url\|--tag\|--note] <query>` | Find bookmarks whose chosen field contains the query. With no flag, every field is searched. |
| `remove <id>` | Delete a bookmark. |
