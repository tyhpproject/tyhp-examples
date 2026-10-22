# Clocks

`ClockShape` is an object shape with `now()`. `FixedClock` matches that shape. `Marker` does not. `describe` accepts any `object` and narrows with `is ClockShape`. The shape check calls the generated `ClockShape()` helper, which `bootstrap.php` loads.

## Install and run

From this directory, with Tyhp and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php help
php build/src/index.php fixed 2020-01-02T03:04:05+00:00
php build/src/index.php other
```

## Commands

| Command | Effect |
| --- | --- |
| `fixed <iso-8601>` | Print that instant in ISO 8601. `fixed 2020-01-02T03:04:05+00:00` prints `2020-01-02T03:04:05+00:00`. |
| `other` | Print `not a clock`. |
