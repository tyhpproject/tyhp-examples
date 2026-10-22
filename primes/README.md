# Primes

Counts how many primes are below a limit. The range is split into two chunks. Each chunk is a `ParallelTask<int>` run with `Parallel::forAsync()` on a two-worker pool. The command awaits the results and adds them up.

This example needs the `pcntl` and `posix` extensions, which `tyhp/parallel` requires.

## Install and run

From this directory, with Tyhp and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php help
php build/src/index.php count 10
php build/src/index.php count 30
```

## Commands

| Command | Effect |
| --- | --- |
| `count <limit>` | Print the number of primes in `[0, limit)`. `count 10` prints `4`. `count 30` prints `10`. |
