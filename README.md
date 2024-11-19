[![stars](https://img.shields.io/github/stars/Pierre-Thibault/backup)](https://github.com/Pierre-Thibault/backup)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
 
# backup

A script to backup a folder as encrypted archives.

## Description

This script backup the folders from the `source` path to the `destination` directory 
[(See Installation)](#Installation).
All folders directly in `source`, not starting with a dot in its name, are backup as its own encrypted 
compressed tar archive except if this folder contains a file named `.nobackup`. Non dot files at source
level are not backup.

The dot files and folders at `source` level are backup in their own separated archive named 
`dot_files.tar.gz.pgp`.

This script ask for the encryption passphrase startup. The passphrase is needed for restoration.

> [!WARNING]
> If the password is forgotten, you won't be able to restore.

## Installation

1. Move `backup_template` to `backup` in some directory in your PATH.
1. Change the `source` and `destination` variables in the script to define the source and the destination of the backup to your licking.
1. Ensure the file is executable.
1. Ensure the dependencies are installed.
1. Ensure `gpg` is configured properly.
1. Ensure the drives needed are mounted.

## Usage

`backup`

## Dependencies

  - bash
  - tar
  - gpg

## Author

Pierre Thibault 2024-11-06

## License

MIT https://opensource.org/license/MIT

## Contributors 🌟

  - Inspired by: https://linuxconfig.org/how-to-create-compressed-encrypted-archives-with-tar-and-gpg

