# ZSH Guide

## Index

1. [Fonts](#fonts)
2. [Colors](#colors)
3. [ZSH](#zsh)

## Fonts

1. Download a patched font from the [Nerd Fonts Github](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts)
2. Install the patched font
    1. User installation
        1. Create **.fonts** directory for the current user: `mkdir ~/.fonts`
        2. Move the font inside: `mv <font> ~/.fonts/`
    2. System-wide installation
        1. Move the font into the system font directory: `mv <font> usr/share/fonts/`
3. Set the font on the terminal

## Colors

Download a shell color scheme from [Gogh](https://github.com/Gogh-Co/Gogh): `bash -c "$(wget -qO- https://git.io/vQgMr)"`.

## ZSH

### Installation and Setup

1. Install zsh: `sudo apt update && sudo apt install zsh`
2. Change the defaut shell: `chsh -s $(which zsh)`
3. Logout and login
4. Follow the wizard or select `0` if you want to configure the shell later with OMZ

### Oh My Zsh

[Oh My Zsh Github](https://github.com/ohmyzsh/ohmyzsh).

#### Installation

1. Install ohmyzsh: `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`

#### Aliases

Create an alias for a command in `.zshrc`: `alias <alias_name> '<command>'`.

#### Plugins

##### Autosuggestions

[Github page](https://github.com/zsh-users/zsh-autosuggestions).

1. Clone the repo: `git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions`
2. Activate the plugin in `~/.zshrc`: `plugins=(zsh-autosuggestions)`

##### Syntax highlighting

[Github page](https://github.com/zsh-users/zsh-syntax-highlighting).

1. CLone the repo: `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting`
2. Activate the plugin in `plugins=(zsh-syntax-highlighting)`

#### Update

Update oh-my-zsh: `omz update`

### Powerlevel10k

[Powerlevel10k Github](https://github.com/romkatv/powerlevel10k).

#### Installation

1. Clone the repo: `git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k`
2. Set `ZSH_THEME="powerlevel10k/powerlevel10k"` in `~/.zshrc`

#### Setup

Setup: `p10k configure`.

#### Update

Update: `git -C ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k pull`
