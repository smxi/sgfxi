# What is sgfxi? #
sgfxi is a self-updating nvidia, ati/amd fglrx, and xorg free driver installer and xorg configuration script written for originally for Debian, but since expanded to also include support for Ubuntu and Arch Linux systems.

Easy to use, updated usually the same day as new nVidia drivers are released. fglrx support is much less reliable because ATI/AMD does not actively support cutting edge software, but it should be good for most fixed pool distributions based on Debian/Ubuntu, and the Debian Stable/Testing/Sid branch, as well as Arches rolling release model.

This project includes the patches used to keep up with latest kernels, and sgfxi includes an automated patch installer as well.

I'm especially interested in getting a little more help on this project, because tracking non free drivers in real time is a fairly tedious, and thankless, project.

## Why sgfxi, and how does it work? ##
Sadly, especially for nvidia cards, non free drivers are a necessary evil.

One of the nice features with sgfxi is that each time you run it, unless some new options are added, it will strip out the old drivers, any found, and update to your new choice, which means that, in the case of ATI cards, you would run say sgfxi -N radeonhd to test how the latest radeonhd works, and it didn't do the job, run: sgfxi (no args) to install the latest non free ati/amd binary run package.

## Also supports standard distro driver install methods ##
Also supports standard Debian/Ubuntu method driver install (using Debian/Ubuntu packages, that is). Note: Debian support for nVidia packages in Testing/Stable varies release to release, and given how complicated the hacks are to create that support automatically, sgfxi will probably never get that support. Too much work to keep up.

Ubuntu non free driver package installs (from their repos that is) should be fine although this varies release to release of these distros, and kernel version to kernel version, and Xorg version to Xorg version.

Other than that, the script is heavily tested, and is used thousands of times per month, with almost total success.

## Script Support and Issues ##
Please use either the Issues tab here (must be a google member, logged in), or, if you prefer, use the script [user forums](http://techpatterns.com/forums/forum-33.html) or for developers, use the [script developer's forums](http://techpatterns.com/forums/forum-32.html).

Also see the [script documentation](http://techpatterns.com/docs/) for beginner to advanced dev options and advice.

## Distro native sgfxi install methods ##
Antix: just run the command: sgfxi
as root and it will download and install the script automatically.

ArchLinux (currently available through aur package pool): yaourt -Sy --aur && yaourt -S sgfxi

Remember to always update sgfxi prior to running it since if you run the Arch package, sgfxi does not autoupdate, as it would normally do if run as the straight script version.

Talk to fester64x2 for any Arch specific packaging concerns or feature requests etc, or just post them on the script forums.