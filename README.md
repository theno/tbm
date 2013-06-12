# Terminal Bookmarks Manager

The *terminal bookmarks manager (tbm)* is a small commandline tool which makes it
easy to switch fast to often used directories.


## Usage

Assumption: *tbm* was installed and the ~/.bashrc was configured as described
below.

Add a bookmark:

    > b .
    > b /path/to/filename/also/possible

Add a bookmark with shortname:

    > b /path/to/a/unhandy/filename fn

List all bookmarks (and change the current dir):

    > b

*tbm* now asks you, where it should change to. Just enter a number.

Change dir to bookmark folder (by number):

    > b 2

Change dir to bookmark folder (by name):

    > b fn

Remove a bookmark:

    > b r fn


## Installation

Copy file *tbm* to a PATH'ed dir, for example on Ubuntu to `~/bin/`.

Tweak your `~/.bashrc`. Change the shortcut to your personal needs:

    alias b=tbm


## Files

### Bookmarks

This is an example bookmarks file. `~/.tbm/bookmarks`:

    /path/to/first/bookmark
    /second/entry/has/also/a/shortname sn
    /the/third/also a
    /another/entry

### Config

The config file of *tbm* is `~/.tbm/config`:

    # If yes: Delete empty lines if an entry within the bookmarks was deleted
    rise_in_rank = no
    # First index
    first_index = 1
