## NVIM

- Install neovim: *sudo pacman -Syu*
- Make neovim alias vim
    - For permanent effect add it to *~/.zshrc*: *echo 'alias vim=nvim' >> ~/.zshrc*
    - For the change to take effect: *source ~/.zshrc*

### nvchad

- Install nvchad-git: *yay -Syu nvchad-git*
    - This will likly fail due to **/usr/share/nvim/archlinux.vim exists in filesystem**
    - Rename this file: *sudo mv /usr/share/nvim/archlinux.vim /usr/share/nvim/old.archlinux.vim*
    - Retry the installation
- Start neovim: *vim*
    - Anser no (N) to **Do you want to install example custom config? (y/N)**
    - Wait for the default plugins to be installed
- Configure neovim
    - Change the theme: Press **spc t h** and search for catppuccin (navigate up and down using **ctrl + p** and **ctrl + n**)
    - Install syntax highlighting: **:TSInstall rust**
        - Check for installed and available syntax highlighting: **:TSInstallInfo**

### Keybindings

- Cheatsheet: **spc c h**
- Change theme: **spc t h**
- Toggle file tree: **ctrl + n**
- Find file:
    - All files: **spc f f**
    - Open files: **spc f b**
- Split window:
    - Horizontal: **:sp**
    - Vertical: **:vsp**
- Tabs:
    - Navigate left/right: **tab**/**shift + tab**
    - Close: **spc x**
- Terminal:
    - Open horizontal: **spc h**
    - Open vertical: **spc v**

#### File tree

- Open/close: **ctrl + n**
- Open file: **enter** or **tabe**
- Open/collapse folder: **enter** or **tab**
- Mark file: **m**
- File system:
    - Create new: **a**
    - Copy/paste: **c**/**p**
    - Rename: **r**
