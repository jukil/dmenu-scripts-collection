# Description

A small bash-script for searching files in $HOME (or elsewhere) using dmenu.

# Features

  * For performance, caches the file list and only updates the list if older than a predefined value (defaults to 5 minutes)
  * Exclude files (defaults to dot-files)
  * Select search directories (defaults to $HOME)

# Example

`$ ./fmenu -i /home/user -t +10`

# Credits

Thanks to isakkarlsson. The script can be found in his [Github repo](https://github.com/isakkarlsson/fmenu).


