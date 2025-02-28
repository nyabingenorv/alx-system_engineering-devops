# alx-system_engineering-devops

## Variables

### Types of variables

- Shell variables are in uppercase characters by convention.
- Bash keeps a list of two types of variables:

#### Global variables

- Global variables or **environment** variables are available in all shells.
- The env or *printenv* commands can be used to display environment variables. These programs come with the **sh-utils package**.

```bash
franky ~> printenv
CC=gcc
CDPATH=.:~:/usr/local:/usr:/
CFLAGS=-O2 -fomit-frame-pointer
COLORTERM=gnome-terminal
CXXFLAGS=-O2 -fomit-frame-pointer
DISPLAY=:0
DOMAIN=hq.garrels.be
```

#### Local variables

- Local variables are **only available** in the current shell.
- Using the `set` built-in command without any options will display a list of all variables (including environment variables) and functions.
- The output will be sorted according to the current locale and displayed in a reusable format.

Below is a diff file made by comparing printenv and set output, after leaving out the functions which are also displayed by the set command:

```bash
franky ~> diff set.sorted printenv.sorted | grep "<" | awk '{ print $2 }'
BASE=/nethome/franky/.Shell/hq.garrels.be/octarine.aliases
BASH=/bin/bash
BASH_VERSINFO=([0]="2"
BASH_VERSION='2.05b.0(1)-release'
COLUMNS=80
DIRSTACK=()
DO_FORTUNE=
EUID=504
```
