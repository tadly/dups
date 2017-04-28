dups
====
Simple shell script to backup (archive) files/directories to a local target while only keeping a set amount of generations.

## Usage
```
$ dups --help
usage: dups [options] [source [...]] [target]

Options:
  -p [prefix]       Prefix to add to the filename.
  -s [suffix]       Suffix to add to the filename.
  -g [generations]  Generations to keep.
                    Set to 0 to keep infinite.
                    Defaults to 3.
  -y, --yes         Don't ask for confirmation.
  --install         Install to system (/usr/bin/dups)
  --uninstall       Uninstall from system (/usr/bin/dups)
  -v, --version     Print version and exit
  -h, --help        Show this help text.

Notes:
  - Deletion of old backups will take the prefix and suffix into
    account. This means neither of these should be dynamic as
    otherwise older version will not be deleted.
```

## Installation
### Manual
```sh
git clone https://github.com/Tadly/dups
./dups/dups --install
rm -rf ./dups

# To uninstall it again
dups --uninstall
```
