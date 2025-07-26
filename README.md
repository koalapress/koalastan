# KoalaStan

Simple PHPStan configuration for KoalaPress projects.

## Installation

In your KoalaPress project:

```bash
composer require --dev koalapress/koalastan
```

## Usage

Create a `phpstan.neon` in your project root:

```neon
includes:
    - vendor/koalapress/koalastan/extension.neon

parameters:
    paths:
        - app/
        - config/
        - resources/
        # Add your custom paths
```

Run PHPStan:

```bash
vendor/bin/phpstan analyse
```

## What's Included

- Pre-generated stubs for KoalaPress Framework
- Pre-generated stubs for Corcel and Acorn
- WordPress-optimized PHPStan configuration
- Sensible defaults for WordPress projects

## Updating Stubs

Stubs are maintained in this repository. When KoalaPress Framework is updated, the stubs will be regenerated and released.


### Generating Stubs

Stubs are generated using a simple docker-compose setup. To generate the stubs, run:

```bash
docker compose up
```

## Requirements

- PHP 8.1+
- PHPStan 1.10+
- KoalaPress project structure

