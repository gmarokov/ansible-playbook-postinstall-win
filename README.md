Ansible playbook: Post Windows installation 
=========
[![Build Status](https://travis-ci.org/gmarokov/ansible-playbook-postinstall-win.svg?branch=master)](https://travis-ci.org/gmarokov/ansible-playbook-postinstall-win)

Post Windows installation Ansible script for provisioning development machine using WSL to run Ansible over WinRM.

## Installation
1. Enable and install WSL
3. Install Ansible on WSL
4. Enable WinRM on Windows

More details about the installation can be found on this [blog post](https://dev.to/gmarokov/configure-your-dev-windows-machine-with-ansible-41aj).

## Usage
Provide Windows username and password when pulling:   
`ansible-pull -U https://github.com/gmarokov/ansible-playbook-postinstall-win.git -e ansible_user=your_win_user -e ansible_password=your_win_user_password`

## Script details 

### Pre tasks
- Install Chocolatey
- Enable hidden files
- Enable file extension
- Uninstall all preinstalled win apps

### Tasks
Install the following packages with Chocolatey: 
 - git
 - notepadplusplus
 - sql-server-management-studio
 - azure-data-studio
 - docker-cli
 - docker-compose
 - vscode
 - visualstudio2019community
 - sourcetree
 - nodejs-lts
 - postman
 - yarn
 - fiddler
 - velocity
 - firefox
 - googlechrome
 - libreoffice
 - lightshot
 - ditto
 - 7zip
 - winscp
 - skype
 - slack
 - spotify
 - donetcore sdk 2.2

### Post tasks
- Reboot
