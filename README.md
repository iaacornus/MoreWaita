# MoreWaita

An Adwaita styled companion icon theme with extra icons for popular apps to fit with Gnome Shell's original icons.
The purpose of this theme is to provide third-party apps with a consistent look and feel in Gnome Shell.

**NB**: This theme requires Adwaita in order to work.

## Installation

### Manual installation

```
git clone https://github.com/MoreWaita-Dev/MoreWaita
cd MoreWaita
sudo ./install.sh
# or ./install.sh
```

### Arch Linux

The package is in [AUR (versioned)](https://aur.archlinux.org/packages/morewaita)
[AUR (git)](https://aur.archlinux.org/packages/morewaita-git). You can use `yay` or whatever AUR package helper.

```bash
yay -S morewaita
# or yay -S morewaita-git
```

### Fedora Linux

The package can be found in [COPR repository](https://copr.fedorainfracloud.org/coprs/dusansimic/themes).

```
dnf copr enable dusansimic/themes
sudo dnf install morewaita-icon-theme
```

## Activation

Either use the `Tweaks` app to choose and activate the icon theme or run the following command:

```
gsettings set org.gnome.desktop.interface icon-theme 'MoreWaita'
```

## Uninstall

Simply chose another theme and then delete the entire `MoreWaita` folder from either `/usr/share/icons/` or
`~/.local/share/icons/` depending on your installation choice above.

# Using custom folder icons

1. Open Files (Nautilus).
2. Find the folder you wish to change the icon for.
3. Right click on the folder.
4. Click on `Properties`.
5. Click on the folder image.
6. Navigate to the MoreWaita installation folder and into the `places` subfolder (typically `/usr/share/icons/MoreWaita/places/scalable/`).
7. Select the icon you wish to use.
8. Click `Open`.
9. Follow the same procedure to revert the icon. Just click `Revert` instead of selecting a new icon in step 7.

![change_folder_icon](assets/demo.png)

# Troubleshooting

### Theme doesn't apply

If the theme doesn't apply try the following command:

### For system-wide installation
`sudo gtk-update-icon-cache -f -t /usr/share/icons/MoreWaita && xdg-desktop-menu forceupdate`

### For local installation
`gtk-update-icon-cache -f -t ~/.local/share/icons/MoreWaita && xdg-desktop-menu forceupdate`

#### Some apps don't get themed

If the theme applies, but a particular app doesn't get themed (and its icon is in MoreWaita), check its respective `.desktop` file. Some apps
have icon paths hardcoded into their `.desktop` file or have a different icon name set there or no icon set at all. This can differ between distros.
If you happen to have such apps, you'll need to copy their `.desktop` files into `~/.local/share/applications` and modify them there providing the
correct icon name. Alternatively, use a menu editor like `MenuLibre` or `Alacarte`.

If your app's `.desktop` file references an icon name not present in MoreWaita's `apps/scalable` folder, please report it in an issue providing the icon name from your system.

# Credits

This theme is built mostly upon the work of Gnome's Adwaita designers and Gnome Circle apps' developers, as well as
Papirus theme designers,  with a touch of tinkering from [@somepaulo](https://github.com/somepaulo), [@dusansimic](https://github.com/dusansimic),
[@julianfairfax](https://github.com/julianfairfax) and others here and there. The theme provides icons for the most popular apps people really
do install and use, and also covers the most frequently installed dependency GUI apps that almost nobody uses (like Avahi browsers, QT Designer,
Software token, etc.).

The goal of MoreWaita is to add to Adwaita, not modify it, and to do roughly what Breeze does for KDE. This theme does not override any Adwaita icons,
nor any Gnome Circle apps icons, nor icons that generally fit into the Adwaita paradigm (like Transmission GTK). Currently, this theme is way less
all-inclusive than many others, but the aim is to be on par with Papirus some day. However, this is (mostly) a one-man hobby effort, albeit with some greatly
appreciated help, so suggestions, requests, PRs and contributions are very welcome. In the meantime, I'll focus on adding icons that the community is requesting.

For most icons, especially branded ones, the general idea is to stay as close as possible to the original icons – to the point of using them in full –
and giving them the distinct Adwaita 'perspective' and general flatness. One thing this theme deviates from is the Gnome colour palette in brand icons
– MoreWaita keeps the brand colours.

This theme is built and tested against vanilla Gnome on Arch Linux. If an icon is in the theme, but is not applying to your app, please open an issue
and mention the icon name referenced in your app's `.desktop` file.

# The Icons
_These screenshots show icons currently in git, versioned releases may be behind_

![apps](assets/apps.png)
![mimes](assets/mimes.png)
![places](assets/places.png)
