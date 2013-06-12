# Terminal Bookmarks Manager

The **terminal bookmarks manager (tbm)** is a small commandline tool which makes it
easy to switch fast to often used directories.


## Usage

Assumption: **tbm** was installed and the `~/.bashrc` was configured as described
below.

Add a bookmark:

    > b .
    > b /path/to/dirname/also/possible/
    > b ./../../relative/path

Add a bookmark together with a nickname:

    > b /path/to/a/unhandy/filename fn

List all bookmarks (and change the current dir):

    > b
    1    /abs/path/to/current/dir
    2    /path/to/dirname/also/possible/
    3    ./../../relative/path
    4 fn /path/to/a/unhandy/filename
    cd to:

**tbm** now waits for your input, where it should change to. Just enter a number
or nickname.

Change dir to bookmark folder (by number):

    > b 2

Change dir to bookmark folder (by name):

    > b fn

Remove a bookmark:

    > b r fn


## Installation

Copy file **tbm** to a PATH'ed dir, for example on Ubuntu to `~/bin/`.

Tweak your `~/.bashrc`. Change the shortcut to your personal needs:

    alias b=tbm


## Files

### Bookmarks

This is an example bookmarks file. `~/.tbm/bookmarks`:

    /path/to/first/bookmark
    /second/entry/has/a/shortname sn
    /the/third/also a
    /trailing/slashes/are/okay/

### Config

The configuration file of **tbm** is `~/.tbm/config`:

    # If yes: Delete empty lines if an bookmarks entry was removed
    rise_in_rank = no

    # First index
    first_index = 1
