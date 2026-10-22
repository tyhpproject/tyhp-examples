# Toolbox

Small commands around the PHP standard library: hashing, the clock, base64, and word counts. The calls are typed through `tyhpdef/php`, and string helpers come from `tyhp/core`.

## Install and run

From this directory, with Tyhp and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php hash sha256 hello
php build/src/index.php now
php build/src/index.php base64 hello
php build/src/index.php words "one two three"
```

## Commands

| Command | Effect |
| --- | --- |
| `hash <algorithm> <text>` | Hash text after checking the name against `hash_algos()`. |
| `now` | Print the current time from `DateTimeImmutable` in ATOM format. |
| `base64 <text>` | Base64-encode text. |
| `words <text>` | Print a word count. |
