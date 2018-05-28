# tibia-launcher

![code size](https://img.shields.io/github/languages/code-size/born2discover/tibia-launcher.svg) ![version](https://img.shields.io/badge/version-1.0.0-blue.svg) ![license](https://img.shields.io/github/license/born2discover/tibia-launcher.svg)

A python utility aimed at simplifying installation, update and launch of the Linux client for MMORPG Tibia.

As opposed to Windows and Mac clients, the Linux client for MMORPG Tibia does not have a launcher applications attached to it and thus does not have an auto-update feature. Hence each time there is an in-game update, Linux users must re-download the game client from the official website. That can become tedious, particularly if one wants to preserve their user configuration files (character options, mini-map files and client options) in-between updates.

This utility aims to fill that gap. It allows for a streamlined process for client installation, update, removal as well as provides functionality to launch the game, install community provided mini-map files and solve one of the most common font-rendering issues.

## Installation

The suggested method of installation is through Git by cloning this repository.

```bash
git clone https://github.com/born2discover/tibia-launcher.git
```

The suggest path for the installation is in your home directory: `~/tibia-launcher`

## Folder structure

The launcher application assumes a certain folder structure for its normal operation, that structure is as follows (assuming `installdir="~/tibia-launcher"`):

- By default the client will be installed in (can be changed by providing --PATH during installaiton): `$installdir/tibia`
- Mini-map files will be located in `$installdir/minimap` and symbolically linked to `$installdir/tibia/minimap`
- Character data files will be located in `$installdir/characterdata` and symbolically linked to *`$installdir/tibia/characterdata`*
- Client configuration will be stored in `$installdir/conf` and will be symbolically linked to `$installdir/tibia/conf`


## Usage

```bash
usage: tibia-launcher [-h] [-v]  ...

A python utility handling installation, update and removal of the Linux Client for MMORPG Tibia

optional arguments:
-h, --help     show this help message and exit
-v, --version  show program's version number and exit

commands:

install        install the latest client from the official website
update         update installed client to the latest version
uninstall      remove installed client and all of its files, this action preserves minimap, characterdata and conf
play           start the game client by invoking the start-tibia.sh scrip
install_maps   install minimap files from TibiaMaps.io project
fontfix        apply infinality font rendering fix
selfupdate     update tibia-launcher from github (requires git)

Homepage: https://github.com/born2discover/tibia-launcher
```

## Removal

In order to remove tibia-launcher from your system, simply delete `~/tibia-launcher` directory. If you want to remove only the client, then use the `uninstall` command.


Notice: As with any open-source program or utility, before installing it on your system, have a look at the source code to get a basic understanding of what the program does and how it does it.