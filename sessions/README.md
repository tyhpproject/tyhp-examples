# Sessions

`Log` implements `IsDisposable`. `open` assigns two logs with `:=`, so they close in reverse order when the method returns. `block` uses a `using` block, so the log closes before `after` is printed.

## Install and run

From this directory, with Tyhp and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php help
php build/src/index.php open
php build/src/index.php block
```

`open` prints the two ready lines, then `closed second`, then `closed first`. `block` prints:

```text
block: inside
closed block
after
```

## Commands

| Command | Effect |
| --- | --- |
| `open` | Print both ready lines, then close the second log and the first log. |
| `block` | Print the inside line, close the log, then print `after`. |
