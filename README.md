Random Patches
==============

This is a collection of my patches for various FOSS projects that are not yet (or will never be)
accepted by upstream.

The patches are organized in the way that makes them easy to use on Gentoo with recent portage
versions -- just copy/symlink the directories in this repository to:

    /etc/portage/patches


Disclaimer:
I'm not responsible for any harm that might be caused by those patches.  Use them at your own risk :)


Amarok
------

*   [Delete files from playlist](https://bugs.kde.org/show_bug.cgi?id=170999)
    
    Adds a context menu with a "Delete Tracks" item to the context menu.  The default action is to
    ask for confirmation, then move to trash.  With Shift-Click, the file is deleted instead, with
    Control-Click, the confirmation is skipped (you can use both).  It is a bit of a hack (I just
    put everything into playlist view) and it will silently fail and remove all selected tracks from
    the playlist even if some of them were not files or could not be deleted, but it is better than
    nothing.
    
    Works with 2.4.1 and latest git

