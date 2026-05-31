# eDefine Symfony Tools

## Installation

```shell
composer require edefine/symfony-tools
```

## Configuration

```shell
cp vendor/edefine/symfony-tools/symfony-tools.ini.dist symfony-tools.ini
nano symfony-tools.ini
```

```ini
SETUP_WRITABLE_DIRS="var/log var/cache" # Directories to which web server should have writable access
```

## bin/setup

Sets up the environment:
1. Sets correct permissions to writable directories (**SETUP_WRITABLE_DIRS** from config)

```shell
bin/setup
```

## bin/rebuild

Rebuilds local instance:
1. Drops schema (full database)
2. Recreates schema
3. Loads fixtures
4. Rebuilds frontend
5. Clears cache

For usage see:
```shell
$ bin/rebuild -u

Usage:
  bin/rebuild [options]

Rebuild Options:
  -e|--env ENV  Run rebuild for given environment (default: dev)
  -f|--frontend Rebuilds frontend

Miscellaneous Options:
  -u|--usage    Output this message
```