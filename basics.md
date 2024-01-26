## Enable Bluetooth

- Check that *bluez* and *bluez-utils* are installed (sudo pacman -Syu bluez bluez-utils)
- Enable and start *bluetooth.service* (sudo systemctl enable bluetooth.service --now)

## Install packages

Installing packages: *sudo pacman -Syu*
Removing packages: *sudo pacman -Rns*

### Basic usefull packages

- neovim
- btop

### Coding stuff

- code
- devtoolsss
- rustup

### SSH key

#### Generate key

First create an SSH key using *ssh-keygen -t ed25519 -C "my@email.com"* and Apress enter again to save the key to its default location.
For the passphrase enter your login password.
With some additional setup this allows your SSH Key to be added to an SSH Agent on login.

#### Add SSH Keys to Agent on login

Create the file **~/.config/autostart/ssh-add.dektop** and give it the following content:

[Desktop Entry]
Exec=ssh-add -q
Name=ssh-add
Type=Application

Following this the package ksshaskpass has to be installed using *sudo pacman -Syu ksshakspass*.
Now create the file **~./config/environment.d/ssh_askpass.conf** and give it the following content:

SSH_ASKPASS=/usr/bin/ksshaskpass
SSH_ASKPASS_REQUIRE=prefer

#### Adding new keys

After creating new SSH Keys they have to be added to the SSH Agent using *ssh-add /path/to/new/key </dev/null*.
If the key has another name/location than the default SSH Keys its name has to be specified in the **ssh-add.desktop** file.
For a key at **.ssh/my_new_key** the **Exec** value has to be set to **Exec=ssh-add -q .shh/my_new_key**.

## Git setup

Execute the following commands to have a working git client with some nice to have aliases:

- git config --global user.email "my@mail.com"
- git config --global user.name "My Name"
- git config --global alias.graph "log --oneline --graph"
- git config --global alias.ciff "diff --cached"
