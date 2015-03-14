![http://gource.googlecode.com/svn/trunk/gource-logo.png](http://gource.googlecode.com/svn/trunk/gource-logo.png)

Gource is a software version control visualization tool.

<a href='http://www.youtube.com/watch?feature=player_embedded&v=NjUuAuBcoqs' target='_blank'><img src='http://img.youtube.com/vi/NjUuAuBcoqs/0.jpg' width='425' height=344 /></a>

See more of Gource in action on the [Videos](http://code.google.com/p/gource/wiki/Videos) page.

## Introduction ##

Software projects are displayed by Gource as an animated tree with the root directory of the project at its centre. Directories appear as branches with files as leaves. Developers can be seen working on the tree at the times they contributed to the project.

Currently Gource includes built-in log generation support for **Git**, **Mercurial**, **Bazaar** and [SVN](http://code.google.com/p/gource/wiki/SVN) (as of **0.29**). Gource can also parse logs produced by several third party tools for [CVS](http://code.google.com/p/gource/wiki/CVS) repositories.

## Synopsis ##

view the log of the repository (Git, SVN, Mercurial and Bazaar) in the current path:

```
gource
```

## Donations ##

If you like Gource and would like to show your appreciation and encourage future work on this and other open source projects by the author, please consider making a donation!

[![](https://www.paypal.com/en_US/i/btn/btn_donate_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=TZYLY4VTKC9TN&lc=NZ&item_name=Gource&currency_code=USD&bn=PP%2dDonationsBF%3abtn_donate_LG%2egif%3aNonHosted)

<a href='Hidden comment: 

*Bitcoin*: 15WP34zkaZFJCyzCAKLt9qrWSvDuBN7XLv

http://gource.googlecode.com/svn/trunk/gource-qr.png

'></a>

## Related Software ##

You may also want to check out [Logstalgia](http://code.google.com/p/logstalgia/), a web server access log visualization tool.

## News ##

### 16 October 2014 ###

Gource **0.43** has been released to fix a minor build issue with Boost on multi-arch Linux systems.

There are no other changes so if you're not affected by this you can stick with 0.42.

Changes since 0.42:
  * Updated boost autoconf macros to fix multi-arch detection.

Downloads:

  * [gource-0.43.tar.gz](https://github.com/acaudwell/Gource/releases/download/gource-0.43/gource-0.43.tar.gz)

### 23 September 2014 ###

I've been nominated for this years [New Zealand Open Source Awards](http://www.nzosa.org.nz/) in the [people's choice](http://www.nzosa.org.nz/peoples-choice) category.

Please head [there](http://www.nzosa.org.nz/peoples-choice) and give **Andrew Caudwell's contribution to data visualization** your vote if you'd like to see me win the award.

Thanks!

Andrew

### 9 May 2014 ###

Gource **0.42** fixes some bugs introduced in 0.41 affecting Mercurial, Bazaar support and date range filtering.

Changes since 0.41:
  * Fixed bzr log command when no start date was specified (chrisf).
  * Fixed hg log commit order when date range specified.
  * Fixed hg log command line on Windows.
  * Fixed parser bug in date range filtering code.

Downloads:

  * [gource-0.42.tar.gz](https://github.com/acaudwell/Gource/releases/download/gource-0.42/gource-0.42.tar.gz)
  * [gource-0.42-setup.exe](https://github.com/acaudwell/Gource/releases/download/gource-0.42/gource-0.42-setup.exe)
  * [gource-0.42.win32.zip](https://github.com/acaudwell/Gource/releases/download/gource-0.42/gource-0.42.win32.zip)

### 14 April 2014 ###

Gource **0.41** has been released.

You can now specify a date range directly with --start-date and --stop-date (using 'YYYY-MM-DD hh:mm:ss' ISO format).

Gource now uses SDL 2.0 when available, providing much better multi-monitor support.

Changes since 0.40:
  * Multi-monitor support using SDL 2.0 when available.
  * SDL 1.2 support is deprecated.
  * Full screen mode now uses desktop resolution by default.
  * Added --start-date, --stop-date 'YYYY-MM-DD hh:mm:ss' options.
  * Added --dir-name-depth option.
  * Changed --file-idle-time default value to 0.
  * Changed screenshot format to PNG.

Downloads are now hosted on Github as Google Code no longer accepts adding new downloads:

  * [gource-0.41.tar.gz](https://github.com/acaudwell/Gource/releases/download/gource-0.41/gource-0.41.tar.gz)
  * [gource-0.41-setup.exe](https://github.com/acaudwell/Gource/releases/download/gource-0.41/gource-0.41-setup.exe)
  * [gource-0.41.win32.zip](https://github.com/acaudwell/Gource/releases/download/gource-0.41/gource-0.41.win32.zip)

If you package Gource for a distro, please update the dependencies to use SDL 2 instead of SDL 1.2.

### 26 April 2013 ###

Gource **0.40** has been released.

This version finally adds support for [captions](http://code.google.com/p/gource/wiki/Captions) (as seen in the recent [Minecraft](http://www.youtube.com/watch?v=zRjTyRly5WA) Gource video).

On Windows I've tried to improve the command prompt integration so Gource no longer creates its own separate console window (unless launched directly).

I've also made a [Windows installer](http://gource.googlecode.com/files/gource-0.40-setup.exe) which can set up Gource to be available on command prompt for you (NOTE: if you have previously manually added Gource to your PATH you will want to remove this before using the installer).

Changes since 0.39:
  * Added caption support.
  * Improved command line interoperability on Windows.
  * Fixed directory deletion short circuiting processing the rest of a commit.
  * Fixed issue loading non-ascii user image filenames on windows.
  * Ignore UTF-8 byte order mark at the start of lines in custom log files.
  * Fix to boost macros for Macs and non-GNU systems (mistydemeo).
  * Autotools improvements (flameeyes).


### 11 January 2013 ###

Gource **0.39** has been released.

This fixes some minor bugs and packaging issues, plus one new feature to allow custom logs to change file colours over time.

Changes since 0.38:
  * Fixed blurry non power of 2 logos.
  * File colour changes now supported in custom logs (rmyorston).
  * Fixed building against Boost 1.50 (svenstaro).
  * Updated boost autoconf macros (flameeyes).
  * Autogen script (matthiaskrgr).

### 23 April 2012 ###

The Windows build of Gource **0.38** I put up the other day didn't statically link gcc/stdc++ so if you got that you probably saw an error about missing symbols or DLLs.

Here is an [updated build of Gource 0.38](http://gource.googlecode.com/files/gource-0.38-1.win32.zip) for Windows.

### 20 April 2012 ###

Gource **0.38** has been released.

I redrew the sprites for this version to make them a bit more detailed. The application window is now resizable and you can toggle fullscreen mode with alt-enter.

Changes since 0.37:
  * New high quality sprites.
  * Fullscreen toggle with alt + enter.
  * Window is now resizable. -WIDTHxHEIGHT! creates a non-resizable window.
  * Lowered minimum zoom distance.
  * Use AM\_CPPFLAGS in Makefile.am to allow passing custom CPPFLAGS.
  * Don't add files that match the path of a known directory.
  * Fixed divide by zero in text shader causing artifacts on some video cards.
  * Recursively search for repository directory when log-format not specified (thanks to Jörg Bachmann for original concept / prototype).
  * New dependency on Boost Filesystem.
  * Doubled the maximum zoom out distance.
  * Allow negative timestamps before 1970 in custom log (artzub).
  * Fix for UTF8-CPP checked.h compilation issue (vszakats).
  * Fixed bug causing missing characters in text.
  * Fixed --highlight-users option not using highlight-colour.
  * highlight-colour default changed to white.
  * Added --selection-colour option (applied to selected users and files).
  * Added --dir-colour option (applied to directories).

There are some new dependencies for building this version:
  * [GLM](http://glm.g-truc.net/) 0.9.3 (header only library)
  * [Boost Filesystem](http://www.boost.org/doc/libs/1_41_0/libs/filesystem/doc/index.htm) >= 1.46

### 19 September 2011 ###

Gource **0.37** has been released, fixing a few bugs with timestamps and directory deletion.

Changes since 0.35:
  * Fixed SVN log GMT timestamp conversion.
  * Fixed issue with sub-dirs of deleted dir not being removed in some cases.

### 27 June 2011 ###

Gource **0.35** is out. This release fixes a few bugs and handles truncation on the file extension key display (enabled with --key or pressing K).

Changes since 0.34:
  * Added long file extension truncation handling to file key (--key).
  * Treat changes in Mercurial log files with the same time/user as one commit.
  * Fixed handling of spaces in directory names with Mercurial.
  * Fixed --font-colour option.

### 14 May 2011 ###

Gource **0.34** has been released.

Gource now features an OpenGL 2.0 rendering pipeline which dramatically improves performance on large repositories, while still maintaining legacy support for older graphics cards.

A significant visual improvement in this version is the elimination of 'banding' artifacts in bloom via use of shaders where OpenGL 2.0 support is available (you can toggle the older render with P-key to see the difference).

Packagers may want to note that this release no longer depends on FTGL and instead uses a custom font library that calls freetype2 directly.

Changes since 0.32:
  * Now using VBOs and shaders for faster rendering when OpenGL 2.0 is available.
  * Eliminated bloom colour banding artifacts (requires OpenGL 2.0).
  * New font rendering library derived from FTGL (FTGL no longer required).
  * Single pass font/shadow rendering (with lots of help from Chris Forbes).
  * Added --no-vsync option.
  * Fixed bug where tree is out of alignment with object positions in windowed mode due to using the wrong display dimensions internally.
  * Removed default max-files limit.
  * Added --hide root option to not draw branches from the root directory.
  * Fixed log parsing of Bazaar merges and tagged commits.
  * --output-custom-log now skips unparsed log entries instead of exiting.

### 2 March 2011 ###

Gource **0.32** has been released to fix a bug in the camera tracking of users (camera gets progressively further away over time) introduced in 0.29.

### 17 February 2011 ###

Gource **0.31** has been released as a minor update to allow building Gource with the system library of [TinyXML](http://www.grinninglizard.com/tinyxml/) (used by the SVN and cvs2cl parsers) instead of the bundled version.

### 14 February 2011 ###

Gource **0.30** has been released.

This version fixes a couple bugs in the recently added SVN log support.

Changes since 0.29:
  * Fixed crash when SVN log entry contains no 'paths' element.
  * Handle directory deletion (happens in SVN logs).

### 13 January 2011 ###

Gource **0.29** has been released.

Changes since 0.28:
  * SVN built-in support.
  * cvs2cl log support (cvs-exp support is now deprecated).
  * Made camera behaviour when zooming and selecting objects more intuitive.
  * Improved interactive performance.
  * Added file extension key (--key or toggled with 'K').
  * Added mouse-over tool tips.
  * Added --highlight-colour option.
  * Added --hash-seed option. The S key now randomizes colours.
  * Added --output-custom-log option.
  * Exposed --time-scale option (previously only available interactively).
  * Removed arbitrary 1024 maximum length limit for log lines.
  * Fixed two file colouring bugs (quoted files from git, period in file path).
  * Fix handling of avatars for UTF-8 usernames on MACOSX (Christian Köstlin).
  * Recover from video mode failing to set due to multi-sampling (Siddhesh Poyarekar).