# Usage
Run dmenu with custom aliases support, sorted by recent use, using the `dmenu_recent_aliases` script:

```bash
dmenu_recent_aliases -fn 'Noto Sans-10' -sb '#3A81CC' -nb '#ffffff' -nf '#000000'
```

By default, aliases and functions need to be stored in `~/.zsh_aliases`. The location can be changed in the script:

```bash
cache=~/.cache/dmenu_run
freq=~/.dmenu_history
aliases=~/.zsh_aliases
```

Over time, `dmenu_recent_aliases` will store your most frequently used files in `~/.dmenu_history`. By default, these entries will persist even on removal of applications. In order to clean your history, you have to manually run the following command:

```bash
$ dmenu_recent_aliases remove <application_name>
```

# Contributions

* Samee Zhaur and his [propsed patch](https://groups.google.com/forum/#!topic/wmii/Mvv5i2CPo7A)
* [dennis123123](https://bbs.archlinux.org/profile.php?id=26975) for his custom functions support
* Ewan Coder for his [re-write](https://github.com/ewancoder/dotfiles/blob/master/bin/dm)
