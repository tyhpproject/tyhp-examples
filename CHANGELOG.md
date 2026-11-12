# Changelog

Notable changes to the Tyhp example applications in this repository. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/). The examples are not versioned; releases are dated by push to `main`.

## [Unreleased]

### Changed

- chirper: chirps use `tyhp/rhetoric` (`App\Data\Chirp`, `Author`, `ChirpContext`); `User` stays Eloquent for auth. `config/rhetoric.php` registers the context. `composer.json` requires `tyhp/rhetoric` 805.0.0.
- todo-cli: file structs are constructed with bracket initializers (`new TaskRecord[field => value]`, `new TaskFile[]`). Commands and saved JSON are unchanged. Requires a Tyhp compiler that accepts that form.
- bookmarks: file structs are constructed with bracket initializers (`new BookmarkRecord[field => value]`, `new BookmarkFile[]`). Commands and saved JSON are unchanged. Requires a Tyhp compiler that accepts that form.
- expenses: file structs are constructed with bracket initializers (`new ExpenseRecord[field => value]`, `new ExpenseFile[]`). Commands and saved JSON are unchanged. Requires a Tyhp compiler that accepts that form.
- contacts: file structs are constructed with bracket initializers (`new ContactRecord[field => value]`, `new ContactFile[]`). Commands and saved JSON are unchanged. Requires a Tyhp compiler that accepts that form.
- inventory: file structs are constructed with bracket initializers (`new ItemRecord[field => value]`, `new ItemFile[]`). Commands and saved JSON are unchanged. Requires a Tyhp compiler that accepts that form.
- shortlinks: file structs are constructed with bracket initializers (`new LinkRecord[field => value]`, `new LinkFile[]`). Commands and saved JSON are unchanged. Requires a Tyhp compiler that accepts that form.
- results: file structs are constructed with bracket initializers (`new TicketRecord[field => value]`, `new TicketFile[]`). Commands and saved JSON are unchanged. Requires a Tyhp compiler that accepts that form.
- recipes: file structs are constructed with bracket initializers (`new IngredientRecord[field => value]`, `new RecipeRecord[field => value]`, `new RecipeBoxFile[]`). Commands and saved JSON are unchanged. Requires a Tyhp compiler that accepts that form.

## 2026-11-04

### Changed

- All examples: require `tyhp/compiler` `805.1.2-beta.4`.
- routes: `Paths::items(string $resource)` replaces `widgets()` and `orders()`, building the path with one interpolation that matches the `api/${string}/items` template type. The commands and output are unchanged. Requires Tyhp `805.1.2-beta.4`.
- files: `writeFile` is an `async` function returning `void`, run directly with `EventLoop::run`. The `write` output is unchanged. Requires Tyhp `805.1.2-beta.4`.

### Fixed

- All examples: the top-level README describes `composer update` correctly (it resolves versions from Packagist and rewrites `composer.lock`) and points to `composer install` for the locked versions.

## Baseline - 2026-10-26

Tracking starts at commit `8f52a9e`. Earlier changes are not listed.
