# eDefine Symfony Tools

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