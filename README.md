This is a configured version of the original synth-shell (https://github.com/andresgongora/synth-shell). Only critical information is provided in this document. Refer to original repo for more information.

- **Key changes**
  - better-ls have been updated. 
  - synth-shell-prompt have been configured with monokai theme.
  - setup.sh have been updated to only install better-ls and synth-shell-prompt. 

<br/><br/>



<!--------------------------------------+-------------------------------------->
#                                     Setup
<!--------------------------------------+-------------------------------------->

### Automatic setup

The included [setup script](setup.sh) will guide you step by step through the
process and let you choose what features to install. During this setup, you can
choose to install synth-shell for your user only (recommended) or system-wide
(superuser privileges required). To proceed,
and enter the following into your terminal:
```
git clone git@github.com:leowyy99/synth-shell.git
chmod +x synth-shell/setup.sh
cd synth-shell
./setup.sh
```

Only better-ls and synth-shell-prompt will be installed. Other features will require the original setup script.

Note that for `fancy-bash-prompt.sh` you might also need to have the [power-line fonts](https://github.com/powerline/fonts) package installed. You can install the package as follows (the exact name of the package varies from distro to distro):

* ArchLinux: `sudo pacman -S powerline-fonts`
* Debian/Ubuntu: `sudo apt install fonts-powerline`

### Configuration/customization
You can configure your scripts by modifying the corresponding configuration
files. You can find them, along the example configuration files, in the following directories, (depending on where you installed **synth-shell**):

* Current-user only: `~/.config/synth-shell/`
* System wide: `/etc/synth-shell/`



### Uninstallation
1. Edit `~/.bashrc` and remove the lines referring to synth-shell, usually
at the bottom of the file. If you want to temporarily disable the script, you can
just comment them by placing `#` in front.
```
vim ~/.bashrc
```

2. Remove the folder containing the script, usually in your home folder under 
`~/.config/synth-shell/`.
```
rm -r ~/.config/synth-shell/
```



<br/><br/>



<!--------------------------------------+-------------------------------------->
#                                    Overview
<!--------------------------------------+-------------------------------------->

### fancy-bash-prompt.sh
Adds colors and triangular separators to your bash prompt, and if the current
working directory is part of a git repository, also git statuses and branches.
For best results, consider installing (and telling your terminal to use) 
the `hack-ttf` font alongside the powerline-fonts (the later is required for
the separators).

As for the git status info, `fancy-bash-prompt.sh` prints an additional, fourth 
separator with the name of the current branch and one of the following icons
to indicate the state of the repository (can be changed in the config file):

|          Local-Upstream          | Local branch has no changes | Local branch is dirty |
|:--------------------------------:|:---------------------------:|:---------------------:|
|            Up to date            |                             |           !           |
|     Ahead (you have to push)     |              △              |           ▲           |
|     Behind (you have to pull)    |              ▽              |           ▼           |
| Diverged (you have to pull-push) |              ○              |           ●           |



### better-ls.sh
Makes `ls` print more text, but nicely formatted. When called, `ls` will now list
all files (`-la`), sort folders first, add colors to output, and list hidden
files last after a quick separator. However, if you chose to call `ls` with your
 own parameters (e.g. `ls -l`) it will revert to the default behavior except
for color and sorting options.

<br/><br/>


<br/><br/>



<!--------------------------------------+-------------------------------------->
#                                     About
<!--------------------------------------+-------------------------------------->

This version of synth-shell is done up to fit my personal preference of monokai 
themed terminal and to make use of the upgraded `ls`. 



<br/><br/>



<!--------------------------------------+-------------------------------------->
#                                    License
<!--------------------------------------+-------------------------------------->

Copyright (c) 2014-2021, Andres Gongora - www.andresgongora.com

* This software is released under a GPLv3 license.
  Read [license-GPLv3.txt](LICENSE),
  or if not present, <http://www.gnu.org/licenses/>.
* If you need a closed-source version of this software
  for commercial purposes, please contact the [authors](AUTHORS.md).
  
 <!--------------------------------------+-------------------------------------->
#                                    Ackowledgements
<!--------------------------------------+-------------------------------------->

* Andres Gongora https://github.com/andresgongora/synth-shell
