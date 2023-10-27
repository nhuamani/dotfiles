<p align="center">
    <img width="200" alt="Alacritty Logo" src="https://raw.githubusercontent.com/alacritty/alacritty/master/extra/logo/compat/alacritty-term%2Bscanlines.png">
</p>

# Alacritty

## Install

### Debian

### Arch

``` sh
sudo pacman -S alacritty

```

## fonts
You can also just manually place fonts here if you want them to be installed system wide:

`/usr/share/fonts`

copy folder with
`sudo mv Downloads/Mononoki /usr/share/fonts`

https://github.com/athityakumar/colorls
https://github.com/sebastiencs/icons-in-terminal

## Config

.config/.alacritty.yml
``` yml
opacity: 0.9

font:
    normal:
        # Default:
        #   - (macOS) Menlo
        #   - (Linux/BSD) monospace
        #   - (Windows) Consolas
        family: mononoki Nerd Font
        style: Regular
    bold:
        family: mononoki Nerd Font
        style: Bold
    italic:
        family: MesloLGS Nerd Font
        style: Italic
    size: 12.0

```


