# Todo list

A file-backed command-line todo list. Tasks are stored as JSON (the `TODO_FILE` environment variable, or `todos.json` in the current directory).

Tyhp features in this example: classes, a backed enum, structs, nullable returns, string methods from `tyhp/core`, and `jsonTryDecodeAs<T>()` to load JSON into a struct.

## Install and run

From this directory, with [Tyhp](https://tyhplang.com) and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php help
php build/src/index.php add Buy milk
php build/src/index.php list
php build/src/index.php done 1
```

`composer update` installs `tyhp/core` and the other runtime packages `tyhp init` records. `tyhp build` type-checks `src/` and writes PHP under `build/`.

## Commands

| Command | Effect |
| --- | --- |
| `add <title>` | Add a task. Extra words are part of the title. |
| `list [--open]` | Print id, status, and title. `--open` hides done tasks. |
| `done <id>` | Mark a task done. |
| `reopen <id>` | Mark a task open. |
| `remove <id>` | Delete a task. |
