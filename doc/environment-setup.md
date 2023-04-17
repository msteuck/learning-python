# How to set up dev environment

We'll use Windows Subsystem for Linux 2, so that everything should work in Linux as well, since Linux is generally the preferred ML/DL/AI dev environment.

[One resource](https://towardsdatascience.com/how-to-create-perfect-machine-learning-development-environment-with-wsl2-on-windows-10-11-2c80f8ea1f31) for environment setup.

## Set up Windows first

### Windows Git

- Install Git
  - Use VS Code as Git's default editor
  - Override default branch name to "main" instead of "master"
  - PATH environment: Git from the command line and also 3rd-party software
  - Use bundled OpenSSH
  - HTTPS transport backend: native Windows Secure Channel library
  - Line endings: checkout Windows-style, commit Unix-style
  - Terminal emulator: Use Windows' default console window
  - Default behavior of git pull: "Default (fast-forward or merge)
  - Credential manager: Use the default cross-platform git credential manager
  - Extra options: yes to enable file system caching, no to enable symbolic links
  - Enable experimental support for pseudo-consoles
  - Enable experimental built-in file system monitor

- First time using git in VS Code:
  - `git config --global user.email "msteuck@gmail.com"`
  - `git config --global user.name "Mathew Steuck"`

### Install VS Code

## Install Docker Desktop on Windows

[Docker site](https://www.docker.com/).

## Install WSL2

In a command prompt with administrator privileges:

```bash
wsl --install -d Ubuntu
```

## Set up a Linux admin username and password

Stored in lastpass.

## Update and upgrade packages in WSL2

```bash
sudo apt update && sudo apt upgrade
```

## Install VS Code for WSL2

If you have VSCode installed on Windows, you can use it to open any WSL2 folder. You only need to install the [Remote Extension Development Pack extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack).

## Install and set up git for WSL2

In WSL2:

```bash
git config --global user.email "msteuck@gmail.com"
git config --global user.name "Mathew Steuck"
```

Then, on CMD, run `git update-git-for-windows`. Then, on the Ubuntu terminal, run the following command:

```bash
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/bin/git-credential-manager.exe"
```

## Configure Docker for WSL2

This step is straightforward as we've already installed Docker in the beginning. To link Docker Desktop to WSL2, go to Docker Desktop > Settings > Resources > WSL integration and toggle the Ubuntu button to 'on'. Then, press apply & restart the terminal for the changes to take effect.

Afterward, you should be able to run `docker --version` successfully on WSL2 terminal.

## Install Python, pip, and venv for WSL2

```bash
sudo apt update && sudo apt upgrade
sudo apt install python3 python3-pip python3-venv ipython3
```

## Optional: Modify .bashrc to make WSL2 terminal prettier

## Optional: Install CUDA and cuDNN drivers on WSL2
