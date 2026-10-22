# Calls

`shout` uppercases text. The command does not call it directly. It passes `shout(...)` and a named argument bag to `apply`, whose parameter and return types are `__CallableParametersStruct` and `__CallableReturnType`.

## Install and run

From this directory, with Tyhp and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php help
php build/src/index.php shout hello
```

## Commands

| Command | Effect |
| --- | --- |
| `shout <text>` | Print the text in upper case. Extra words stay in the text. |
