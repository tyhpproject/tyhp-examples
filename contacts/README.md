# Contact directory

A file-backed command-line contact directory. People are stored as JSON (the `CONTACTS_FILE` environment variable, or `contacts.json` in the current directory).

Each person has a name, an email, an optional phone number, and an optional company. Phone and company are stored as `?string` (`null` when omitted).

Tyhp features in this example: classes, structs, nullable `?string` properties, string `contains` and `toLower`, and `jsonTryDecodeAs<T>()` to load JSON into a struct.

## Install and run

From this directory, with [Tyhp](https://tyhplang.com) and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php help
php build/src/index.php add "Ada Lovelace" ada@analytical.example 555-0100 "Analytical Engines"
php build/src/index.php add "Grace Hopper" grace@navy.example
php build/src/index.php list
php build/src/index.php find love
php build/src/index.php remove 1
```

Quote a name or company that contains spaces. `composer update` installs `tyhp/core` and the other runtime packages `tyhp init` records. `tyhp build` type-checks `src/` and writes PHP under `build/`.

## Commands

| Command | Effect |
| --- | --- |
| `add <name> <email> [phone] [company]` | Add a person. Phone and company are optional. |
| `list` | Print id, name, email, phone, and company. |
| `find <text>` | List people whose name or email contains the text (case-insensitive). |
| `remove <id>` | Delete a contact. |
