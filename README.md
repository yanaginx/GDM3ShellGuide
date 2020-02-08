There is an easy way to Install/Switch/Remove GDM3 theme using update-alternatives:

```
update-alternatives --install <link> <name> <path> <priority> 
add a group of alternatives to the system.

update-alternatives --config <name>
show alternatives for the <name> group and ask the user to select which one to use.

update-alternatives --remove <name> <path> 
remove <path> from the <name> group alternative.
```

In this example we will change default(Ubuntu 18.04) GDM theme to Yaru:

Install new alternative for GDM3 theme(gdm3.css):
```
sudo update-alternatives --install /usr/share/gnome-shell/theme/gdm3.css gdm3.css /usr/share/gnome-shell/Yaru/gnome-shell.css 15
```

Alternative installed, now we can select wich one to use:
```
sudo update-alternatives --config gdm3.css


There are 2 choices for the alternative gdm3.css (providing /usr/share/gnome-shell/theme/gdm3.css).

  Selection    Path                                               Priority   Status
------------------------------------------------------------
* 0            /usr/share/gnome-shell/theme/Yaru/gnome-shell.css   15        auto mode
  1            /usr/share/gnome-shell/theme/Yaru/gnome-shell.css   15        manual mode
  2            /usr/share/gnome-shell/theme/ubuntu.css             10        manual mode

Press <enter> to keep the current choice[*], or type selection number: 
```
