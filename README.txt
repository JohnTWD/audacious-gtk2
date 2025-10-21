GTK-2 version of the Audacious package.

Based off of the audacious-gtk3 package in AUR 
See https://aur.archlinux.org/packages/audacious-gtk3

I simply changed a few lines so most of the effort goes to the main maintainers.

Perhaps this could be uploaded to the AUR but I don't know how to do that. I
modified the original script to use GTK-2 because I have a theme that I don't
want to bother porting to GTK-3, and it looks really nice on my system (lol).

To install:
```
git clone https://github.com/JohnTWD/audacious-gtk2.git
makepkg -si
```
And then go to https://github.com/JohnTWD/audacious-plugins-gtk2 and install it
in a similar way because it is required for Audacious to run.
