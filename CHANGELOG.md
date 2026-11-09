# Changelog

Notable changes to the Tyhp example applications in this repository. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/). The examples are not versioned; releases are dated by push to `main`.

## [Unreleased]

### Changed

- chirper: chirps use `tyhp/rhetoric` (`App\Data\Chirp`, `Author`, `ChirpContext`); `User` stays Eloquent for auth. `config/rhetoric.php` registers the context. `composer.json` requires `tyhp/rhetoric` 805.0.0.

## 2026-11-04

### Changed

- All examples: require `tyhp/compiler` `805.1.2-beta.4`.
- routes: `Paths::items(string $resource)` replaces `widgets()` and `orders()`, building the path with one interpolation that matches the `api/${string}/items` template type. The commands and output are unchanged. Requires Tyhp `805.1.2-beta.4`.
- files: `writeFile` is an `async` function returning `void`, run directly with `EventLoop::run`. The `write` output is unchanged. Requires Tyhp `805.1.2-beta.4`.

### Fixed

- All examples: the top-level README describes `composer update` correctly (it resolves versions from Packagist and rewrites `composer.lock`) and points to `composer install` for the locked versions.

## Baseline - 2026-10-26

Tracking starts at commit `8f52a9e`. Earlier changes are not listed.
