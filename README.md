# Tester skeleton

A Nette application skeleton with Nette Tester and the Contributte QA toolchain.

## Requirements

- PHP 8.4 or newer
- [Composer](https://getcomposer.org/)

## Tester quick start

```bash
composer create-project contributte/tester-skeleton acme
cd acme
make init
make setup
```

Composer installs the dependencies. `make init` creates `config/local.neon` from `config/local.neon.example`, and `make setup` creates writable `var/tmp` and `var/log` directories.

## Local development

```bash
make dev
```

Open [http://localhost:8000](http://localhost:8000). The development server uses `www/` as its document root.

In another terminal, verify the visible bundled page and run its tests:

```bash
curl -s http://localhost:8000 | grep -F 'Hello!'
# 	Hello!
make tests
```

## Configuration

Application configuration is in `config/config.neon`. Keep machine- or environment-specific settings in the ignored `config/local.neon` file.

## Quality assurance

```bash
make qa
```

`make qa` runs coding-standard and PHPStan checks. `make tests` runs Nette Tester tests from `tests/`.
