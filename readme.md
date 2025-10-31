## install yay
```sh
sudo pacman -S --needed git base-devel && git clone https://aur.archlinux.org/yay.git && cd yay && makepkg -si
```

## install hypr apps
```sh
yay -S hypridle hyprlock hyprpaper hyprshot
```

## install required packages for walker
```sh
yay -S elephant elephant-desktopapplications elephant-calc elephant-runner elephant-files elephant-clipboard elephant-websearch
```

## install swaync for notifications
```sh
yay -S swaync
```

## install waybar
```sh
yay -S waybar
```

## install neovim
```sh
yay -S nvim
```

## list of lsp, formatters, and linters
- typescript-language-server
- tailwindcss-language-server
- css-lsp
- marksman
- rust-analyzer

## install ghostty
```sh
yay -S ghostty
```

## install cliphist, wofi emoji picker, and noto-fonts-emoji
```sh
yay -S cliphist wofi-emoji noto-fonts-emoji
```
## typography
- Download [JetBrainsMono Nerd Font](https://www.nerdfonts.com/font-downloads)
- unzip the file to `/usr/share/fonts`
- fc-cache -fv
- verify with fc-list

OR

```sh
yay -S nerd-fonts # select jet brains nerd font
```

## ghostty config
```conf
background-opacity=0.8
font-family="JetBrains Mono"
```

## install tmux
```sh
yay -S tmux
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm #clone tpm
tmux source ~/.tmux.conf
#remember to install plugins with prefix + I
```

## zsh plugins configuration
```sh
sh -c "$(curl -fsSL https://install.ohmyz.sh)" #install oh-my-zsh
git clone https://github.com/zsh-users/zsh-history-substring-search ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-history-substring-search
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-completions.git ${ZSH_CUSTOM:-${ZSH:-~/.oh-my-zsh}/custom}/plugins/zsh-completions
```
### replace plugins with following:
```sh
plugins=(
    "sudo"
    "git"                     # (default)
    "zsh-autosuggestions"     # (default)
    "zsh-syntax-highlighting" # (default)
    "zsh-completions"         # (default)
)
```

## install nvm  
```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
```

## bluetooth
```sh
yay -S bluez bluez-utils
sudo systemctl start bluetooth
sudo systemctl enable bluetooth
```
## configure with bluetoothctl
```sh
bluetoothctl
power on
agent on
default-agent
scan on
```

## install blueberry for bluetooth control ui
```sh
yay -S blueberry
```

## install pavucontrol
```sh
yay -S pavucontrol
```

### for sddm theme follow [simple-sddm](https://github.com/JaKooLit/simple-sddm)
### install dependencies for simple-sddm
```sh
yay -S qt5-quickcontrols2 qt5-graphicaleffects
```

## install asusctl
```sh
# add repo sign key to pacman-key
sudo pacman-key --recv-keys 8F654886F17D497FEFE3DB448B15A6B0E9A3FA35
sudo pacman-key --finger 8F654886F17D497FEFE3DB448B15A6B0E9A3FA35
sudo pacman-key --lsign-key 8F654886F17D497FEFE3DB448B15A6B0E9A3FA35
sudo pacman-key --finger 8F654886F17D497FEFE3DB448B15A6B0E9A3FA35
```

### check installation guide at [asusctl installation guide](https://asus-linux.org/guides/arch-guide/)

## gtk theme settings
```sh
# install nwg-look for gtk theme settings gui. gtk-engine-murrine dependency for gtk theme
yay -S nwg-look gtk-engine-murrine
```

```sh
yay -S tokyonight-gtk-theme-git
```
OR
### [tokyonight gtk theme github link](https://github.com/Fausto-Korpsvart/Tokyonight-GTK-Theme?tab=readme-ov-file)

## cursor theme
```sh
yay -S bibata-cursor-theme-bin
```

## git configs
```sh
git config --global init.defaultBranch main
git config --global user.email "aryanmgr79@gmail.com"
git config --global user.name "aryan"
git config --global pull.rebase true
```

## install lazygit
```sh
yay -S lazygit
```

## docker installation
```sh
yay -S docker docker-compose docker-buildx
sudo systemctl enable docker.service
sudo systemctl start docker.service
```

## enabling non-root users to run docker commands (docker post installation)
```sh
sudo groupadd docker
sudo usermod -aG docker $USER
# reboot
```
