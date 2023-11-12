# watch-xfce-xfconf - Automate XFCE Configuration!

## Introduction

The `watch-xfce-xfconf` command-line tool allows displaying and watching the xfconf-query
commands of all the XFCE 4 Xfconf settings that are being changed by XFCE programs like
xfce4-settings-manager, thunar, catfish, ristretto, among others.

The `watch-xfce-xfconf` tool is especially useful for users who want to replicate XFCE 4
settings on several computers.

### What is xfconf-query?

The xfconf-query command-line tool allows retrieving, modifying, and creating XFCE 4
Xfconf settings, such as the desktop background, panel preferences, window decorations,
window manager settings, and more.

### How can xfconf-query commands help automate the configuration of XFCE 4?

By displaying the xfconf-query commands, `watch-xfce-xfconf` allows to easily create a
Shell script that can be used to automate the configuration of XFCE 4, which provides
several benefits:
- It saves time and effort by eliminating the need to manually adjust settings on each
  individual machine,
- It reduces the risk of errors and inconsistencies that may arise from manually
  configuring settings on different machines,
- Finally, it allows focusing on other important tasks rather than spending time
  configuring XFCE 4 manually.

## Installation

The watch-xfce-xfconf command-line tool can be installed locally,
in `~/.local/bin/watch-xfce-xfconf`, using pip:
```console
pip install --user watch-xfce-xfconf
```

## Usage

Run xfce4-settings-manager in the background:
```console
xfce4-settings-manager &
```

After that, execute watch-xfce-xfconf:
```console
~/.local/bin/watch-xfce-xfconf
```

Once you begin modifying XFCE 4 settings using xfce4-settings-manager, `watch-xfce-xfconf`
will automatically display the corresponding xfconf-query commands in the terminal. These
xfconf-query commands can be easily copied and pasted into a Shell script, allowing for
quick and efficient automation of XFCE 4 configuration across multiple machines.

## Author and License

The `watch-xfce-xfconf` tool has been written by
[James Cherti](https://www.jamescherti.com/) and is distributed under terms of the
MIT license.

## Features
- Parses XML files that are located in the directory:
  `~/.config/xfce4/xfconf/xfce-perchannel-xml/`,
- Monitors changes in XFCE 4 settings / Xfconf,
- Displays xfconf-query commands with correctly escaped special characters in their
  arguments.

## Links
- [watch-xfce-xfconf @PyPI](https://pypi.org/project/watch-xfce-xfconf/)
- [watch-xfce-xfconf @GitHub](https://github.com/jamescherti/watch-xfce-xfconf/)
- [General information about Xfconf](https://docs.xfce.org/xfce/xfconf/start)
