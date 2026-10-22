# Files

Writes and reads one text file with `tyhp/io`. `write` awaits `File::writeAsync()`. `read` awaits `File::readAsync()`. The file is `FILES_PATH`, or `note.txt` in the current directory.

## Install and run

From this directory, with Tyhp and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php help
php build/src/index.php write hello tyhp
php build/src/index.php read
```

## Commands

| Command | Effect |
| --- | --- |
| `write <text>` | Replace the file with the text and a trailing newline. |
| `read` | Print the file. |
