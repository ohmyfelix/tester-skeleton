# Tester skeleton

A Nette application skeleton with Nette Tester and the Contributte QA toolchain.

## Requirements

- PHP 8.4 or newer
- [Composer](https://getcomposer.org/)

## Create a project

```bash
composer create-project contributte/tester-skeleton acme
cd acme
make init
make project
```

`make init` creates `config/local.neon` from `config/local.neon.example`. `make project` installs Composer dependencies and creates writable `var/tmp` and `var/log` directories.

## Local development

```bash
make dev
```

Open [http://localhost:8000](http://localhost:8000). The development server uses `www/` as its document root.

## Configuration

Application configuration is in `config/config.neon`. Keep machine- or environment-specific settings in the ignored `config/local.neon` file.

## Quality assurance

```bash
make qa
make tests
```

`make qa` runs coding-standard and PHPStan checks. `make tests` runs Nette Tester tests from `tests/`.
