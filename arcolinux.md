# ArcoLinux

## Install
para poder instalar dualboot
realizar el siguiente paso

https://youtu.be/YH9_OoBdHw8?si=FYy2gZxbZQchcn-S
https://arcolinux.com/install-arcolinux-on-windows-11-on-vmware-16/

## update

update – ArcoLinux packages, third-party packages build for ArcoLinux and Arch Linux packages  – DAILY

upall – updating all AUR packages – any package you installed additionally – DAILY

skel – copy/pasting /etc/skel content to your home directory and making a backup of .config folder – MONTHLY

cb – copy/pasting content from /etc/skel/.bashrc to ~/.bashrc + making it work (source) – MONTHLY

sudo mv Downloads/passion.zsh-theme /usr/share/oh-my-zsh/themes
sudo mv Downloads/ultima.zsh-theme /usr/share/oh-my-zsh/themes

For Arch Linux users

update

```alias update='sudo pacman -Syyu'```

skel

```alias skel='cp -Rf ~/.config ~/.config-backup-$(date +%Y.%m.%d-%H.%M.%S) && cp -rf /etc/skel/* ~'```

cb

```alias cb='sudo cp /etc/skel/.bashrc ~/.bashrc && source ~/.bashrc'```

upall

```alias upall='yay -Syu --noconfirm'```


### Search Package
```pamac search firefox```

qtile cheatsheet



``` bash
sudo pacman -S --needed git && git clone https://aur.archlinux.org/google-chrome.git && cd google-chrome && makepkg -si
```


### Config Promp zsh

config file '.zshrc'

![unix color table](https://i.stack.imgur.com/xjBuI.png "color Unix table")


``` bash
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion


get_node_version() {
  echo "Node → $(node --version)"
}

get_npm_package_version() {
  local JSON=''
  if [[ -f 'package.json' ]]; then
    echo "npm → $(npm --version)"
  fi
}


PROMPT='%F{green}%*%f %F{blue}%~%f %F{red}${vcs_info_msg_0_}%f$ '

RPROMPT='$FG[196] $(get_npm_package_version) $FG[046] $(get_node_version) %{$reset_color%}'
```