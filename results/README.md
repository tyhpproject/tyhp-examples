# Ticket desk

A small helpdesk stored as JSON (`TICKETS_FILE`, or `tickets.json`). Missing tickets come back as a failed `Result<T>` instead of an exception.

Tyhp features in this example: generic classes (`Result<T>`, `MemoryRepository<T>`), a generic `map` method, structs, a backed enum, and `jsonTryDecodeAs<T>()`.

## Install and run

From this directory, with Tyhp and PHP 8.5 on your PATH:

```bash
composer update
tyhp build
php build/src/index.php add ada "Printer jam"
php build/src/index.php list
php build/src/index.php show 1
php build/src/index.php close 1
```

## Commands

| Command | Effect |
| --- | --- |
| `add <requester> <title>` | Open a ticket. |
| `list` | Print every ticket. |
| `show <id>` | Print one ticket. |
| `close <id>` | Close a ticket. |
