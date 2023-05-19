# Change Alpha

A patch that allows for updating terminal transparency natively.

### Description

This patch is an extension to the [alpha](https://st.suckless.org/patches/alpha) patch, 
which _must_ be applied prior. 

### Notes

This patch assumes that the alpha variable is a float, which was only updated in alpha 
patch version 0.8.2 i.e., 0.8.2 is the minimum compatible version.

### Purpose

Later versions of the default alpha patch provide a method of changing window opacity via
the -A flag, however, with no method of querying the current alpha level, it is difficult
to write scripts which increment or decrement this value. It's usually possible to update, 
the opacity via your compositor, but not all compositors support this, and even if they do, 
your setup is still less portable at the end of the day. The 
[transset-df](https://aur.archlinux.org/packages/transset-df) package 
located in the AUR is the closest I've come to changing opacity on a per-window basis, 
however, it still requires writing a script and binding that script to some keys using a 
keybinding manager of some sort. Not to mention, it's fatal flaw - you cannot increase the 
opacity beyond the default value set with the alpha patch.

### Download

This patch is to be applied after you have already applied the alpha patch (version 0.8.2 or 
greater):

[st-changealpha-0.1.diff](st-changealpha-20230519-.diff)

### Author 

Neil Kingdom - <neil@neilkingdom.xyz>
