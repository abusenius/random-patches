Random Patches
==============

This is a collection of my patches for various FOSS projects that are not yet (or will never be)
accepted by upstream.

The patches are organized in the way that makes them easy to apply on Gentoo using the "user
patches" feature of portage -- just copy/symlink the directories in this repository to:

    /etc/portage/patches

See also the [bugreport](http://bugs.gentoo.org/show_bug.cgi?id=349707#c11).
Unfortunately, this method does not work with all ebuilds, in this case, I also provide a patched
ebuild.


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
    
    Works with 2.4.3 - 2.8

*   [DBus extension "Rating"](https://bugs.kde.org/show_bug.cgi?id=325021)
    
    Adds a DBus interface for reading and setting rating of the current track. This adds a new
    property:

    property readwrite int org.kde.amarok.Mpris2Extensions.Player.Rating

    to the org.mpris.MediaPlayer2.amarok /org/mpris/MediaPlayer2 interface.

    Works with 2.7 - 2.8


Coreutils
---------

*   [Progress bar for cp and mv](http://lists.gnu.org/archive/html/bug-coreutils/2003-08/msg00114.html)
    
    Adds a progress bar (command line option: -g) to "cp" and "mv"
    
    This patch was included by default in Gentoo some years ago, but was dropped from the patchset
    because the upstream did not want to accept it.
    I keep the patch up-to-date.
    
    Coreutils ebuild does not apply user patches
    
    Works with 8.21 - 8.22


