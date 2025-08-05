## Night Light Feature in Hyprland

When using **Gnome** or **KDE** , we use **Night light** option present in settings:

**KDE**
![KDE Plasma 5.17: Thunderbolt, X11 Night Color and Redesigned Settings - KDE  Community](https://kde.org/announcements/plasma/5/5.17.0/night-color.png)


**GNOME**

![Night Light Slider - GNOME Shell Extensions](https://extensions.gnome.org/extension-data/screenshots/screenshot_1276_gNya1IO.png)

Alternative to these there are some software like Redshift that can be used..

## But in Hyprland, apps like Redshift doesn't support.

<a href="https://ibb.co/18sdt3S"><img src="https://i.ibb.co/Gcst4Xh/image.png" alt="image" border="0"></a>

Source: [Redshift -Arch](https://wiki.archlinux.org/title/redshift)

So there is a **configuration tool** called [Hyprshade](https://github.com/loqusion/hyprshade)

**Screenshots:**

**Vibrance**![Vibrance](https://github.com/loqusion/hyprshade/raw/main/.github/assets/vibrance.png)

**Blue light filter**
![Blue Light Filter](https://github.com/loqusion/hyprshade/raw/main/.github/assets/blue-light-filter.png)

To install [AUR- Hyprland](https://aur.archlinux.org/packages/hyprshade) on Arch :

    yay -S hyprshade


To install using pacman 

```
sudo pacman -S --needed base-devel
```
This install baisc Dependencies
```
git clone https://aur.archlinux.org/hyprshade.git
cd hyprshade
makepkg -si
```
 
If your distribution isn't officially supported, you can also install directly
from [PyPI](https://pypi.org/project/hyprshade/) with pip:

```sh
pip install --user hyprshade
```

Or with [pipx](https://pypa.github.io/pipx/):

```sh
pipx install hyprshade
```


## Usage
the command `blue light shader` is the one use to change the screen color temperature.

```text
Usage: hyprshade [OPTIONS] COMMAND [ARGS]...

Commands:
  auto     Set screen shader on schedule
  current  Print current screen shader
  install  Install systemd user units
  ls       List available screen shaders
  off      Turn off screen shader
  on       Turn on screen shader
  toggle   Toggle screen shader
```

Commands which take a shader name accept either the basename:

```sh
hyprshade on blue-light-filter
```

    hyprshade on blue-light-filter
in case you want to increase the color `/usr/share/hyprshade/examples/config.toml` is where you can change the value

If you want to use hyprshade command by using buttons , u can add keybindings in the `.config/hypr/keybindings.conf` file

for example

    bind  = $mainMod, F9, exec, hyprshade on blue-light-filter
    bind  = $mainMod, F7, exec, hyprshade on vibrance

And done!!  Now you can use night light feature on **hyprland**
