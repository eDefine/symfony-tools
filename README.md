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

## bin/setup-file-permissions

Sets up file permissions to writable directories (**SETUP_WRITABLE_DIRS** from config)

```shell
bin/setup-file-permissions
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

## bin/deploy-local

Runs local deploy on production server.

Pass branch name or tag as an argument. Otherwise, "master" will be deployed.

Usage:
```shell
bin/deploy-local user directory [branch or tag]
```