# Tyhp examples

Small applications written in [Tyhp](https://tyhplang.com). Each directory is its own Composer project, created with `tyhp init`, and installs packages from Packagist.

## Install Tyhp

You need PHP 8.5, Composer, and the Tyhp compiler on your `PATH`. These examples require PHP 8.5 because the published `tyhp/core` package does. Install the compiler with the steps in the [Tyhp installation guide](https://tyhplang.com/intro_installation.html), then check it:

```bash
tyhp version
```

`tyhp/core` can use the `mbstring` extension for Unicode string methods. Without it, those methods use byte-oriented PHP functions.

## Run an example

From the example directory:

```bash
composer update
tyhp build
php build/src/index.php help
```

`composer update` installs dependencies from `composer.lock`. `tyhp build` type-checks `src/` and writes PHP under `build/`. Run the commands in that example's README for anything beyond `help`.

## Examples

| Directory | What it is | Tyhp features |
| --- | --- | --- |
| [todo-cli](todo-cli/) | File-backed todo list. | Structs (`with`), `jsonTryDecodeAs<T>()`, `tyhp/core` string methods |
| [bookmarks](bookmarks/) | Bookmark list with tags and search. | Literal type alias `SearchScope`, structs (`with`), `tyhp/core` strings (`trim`, `isEmpty`, `toLower`, `contains`, `split`), `jsonTryDecodeAs<T>()` |
| [expenses](expenses/) | Expense tracker using `decimal` amounts. | Structs (`with`), `decimal` (`\Tyhp\decimal()`, `+=`, `<=`, `format()`), `jsonTryDecodeAs<T>()` |
| [contacts](contacts/) | Contact directory with optional phone and company. | Structs (`with`), `tyhp/core` strings (`contains`, `toLower`), `jsonTryDecodeAs<T>()` |
| [inventory](inventory/) | CSV catalog import, quantity adjustments, and CSV export. | Structs (`with`), string `matches()` and `replace()`, `jsonTryDecodeAs<T>()` |
| [shortlinks](shortlinks/) | Local short-link registry and a string slug extension. No network calls. | String extension method `toSlug()` (`regexReplace`), structs (`with`), `jsonTryDecodeAs<T>()` |
| [config-tool](config-tool/) | Load a `.env` file with `vlucas/phpdotenv` and check that keys are set. | `vlucas/phpdotenv` through its tyhpdef |
| [results](results/) | Helpdesk tickets returned as generic `Result<T>` values. | Generic classes `Result<T>` and `MemoryRepository<T>`, generic `map<U>`, structs (`with`), string `format()`, `jsonTryDecodeAs<T>()` |
| [toolbox](toolbox/) | Hashing, the clock, base64, and word counts through PHP's standard library. | PHP standard library through `tyhpdef/php`, `tyhp/core` strings (`base64Encode`, `wordCount`), `is` type checks |
| [recipes](recipes/) | Recipe box that scales ingredient quantities with `decimal`. | Nested structs (`with`), `decimal` (`\Tyhp\decimal()`, `divide`, `multiply`, `round`, `format`), `jsonTryDecodeAs<T>()` |
| [async-jobs](async-jobs/) | Concurrent greetings. | `async` / `await`, `Promise::delay()`, `Promise::all()` |
| [primes](primes/) | Count primes below a limit in worker processes. | `tyhp/parallel` (`ParallelTask<int>`, `Parallel::forAsync()`), `async` / `await` |
| [files](files/) | Read and write one text file. | `tyhp/io` (`File::readAsync()`, `File::writeAsync()`), `async` / `await` |
| [filters](filters/) | Inspect roster predicates and property paths. | Parsable lambdas (`Expression`, `PropertyPath`) |
| [queues](queues/) | Push strings through a queue and print them in order. | Generic PHP `\SplQueue<string>` |
| [gates](gates/) | Report string length, the PHP line, and the first item. | `declare(php=…)`, `#[\Tyhp\Php]`, `declare(ext=…)` |
| [convert](convert/) | Double a number, uppercase text, and look up an id or email. | Short function syntax, method overloads |
| [vectors](vectors/) | Add, scale, and compare 2D vectors. | Operator overloads (`+`, `*`, `==`) |
| [labels](labels/) | Print a note label. | Trait `extends` / `implements` requirements |
| [sessions](sessions/) | Open logs and close them when the scope ends. | Disposables (`IsDisposable`, `:=`, `using`) |
| [symbols](symbols/) | Print symbol names, defaults, and a type. | `nameof()`, `typeof()`, `default()`, `variable_exists()` |
| [codes](codes/) | Prefix and lowercase text. | `internal` visibility |
| [clocks](clocks/) | Format a clock, or reject an object that is not one. | Object shapes, `is` shape guard |
| [guards](guards/) | Classify a value as a positive int or not. | Custom type guard (`$value is int`) |
| [routes](routes/) | Print API paths checked as a template string. | Template string type `` `api/${string}/items` `` |
| [calls](calls/) | Uppercase text through a generic caller. | `__CallableReturnType`, `__CallableParametersStruct` |
| [chirper](chirper/) | The Laravel Chirper bootcamp, written in Tyhp. | Typed controllers, models, factory, seeder, routes, and tests. Laravel typed through `tyhpdef/laravel-framework` and the Illuminate tyhpdef packages |

## License

Apache License 2.0. See [LICENSE.md](LICENSE.md).
