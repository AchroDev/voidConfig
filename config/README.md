<a name="readme-top"></a>
# README.md

<br />
<div align="center">

<h3 align="center"> Config Files </h3>

  <p align="center">
    These are files specifically made for easily building and deploying systems running Void Linux.
    <br />
  </p>
</div>

## Packages:
1. Update the system and repository ```sudo xbps-install -Sy``` or ```sudo xbps-install -Syu```

2. Using ```xbps``` install the following packages ```xbps-install -S xorg-minimal kde5 kde5-baseapps pulseaudio pipewire wireplumber xorg-fonts dbus elogind mesa-dri xf86-video-qxl nano sddm octoxbps ark chromium okular gwenview spectacle void-repo-nonfree neofetch xmirror fish-shell vlc```

These packages will install the KDE Desktop Environment, enable the "nonfree" repo, and some recommended apps to go along with the new environment.

## Symbolic Links For Services:

Almost ready! After installing the packages above, we will need to enable a few services before they will work correctly. For this we are going to create some symbolic links:

- Enable the ```pipewire``` service with ```ln -s /etc/sv/pipewire /var/service```
- Enable the ```pipewire-pulse``` service with ```ln -s /etc/sv/pipewire-pulse /var/service```
- Enable the ```dbus``` service with ```ln -s /etc/sv/dbus /var/service```
- Enable the ```sddm``` service with ```ln -s /etc/sv/sddm /var/service```
- Enable the ```NetworkManager``` service with ```ln -s /etc/sv/NetworkManager /var/service```

## Reboot
After installing all of the packages and enabling the services, you will need to reboot to save and apply all of the changes. In your shell enter ```sudo reboot``` and when it comes back up, you will be at the login screen.

1. Now, login and update the system again ```sudo xbps-install -Su``` to make sure everything is up to date.
2. Once that completes run ```chsh -s /bin/fish USERNAME``` to swap shells from bash to fish.
3. Close out of your shell, reopen it, and run ```fish_config``` to load the web configurator and choose your theme styles. (Make sure you select to apply the options you pick before closing out of the browser.)

## TODO:// (What are these packages?)
- TODO:// Explain packages