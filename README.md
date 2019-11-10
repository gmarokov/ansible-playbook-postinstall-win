# ansible-win-postinstall
Post Windows installation Ansible script for provisioning dev machine using WSL to run Ansible over WinRM.

## Installation
1. Enable and install WSL
3. Install Ansible on WSL
4. Enable WinRM on Windows
5. Add `[local] 127.0.0.1` to your hosts in `/etc/ansible/hosts`

More details about the installation can be found [here](https://dev.to/gmarokov/configure-your-dev-windows-machine-with-ansible-41aj)

## Usage
Provide Windows username and password when pulling:   
`ansible-pull -U https://github.com/gmarokov/ansible-win-postinstall.git -e ansible_user=your_win_user -e ansible_password=your_win_user_password`

## Script details 

### Pre tasks
- Install Chocolatey

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

### Post tasks
- Reboot

## Todos
- Remove default apps
- Enable hidden files
- Enable file extensions
- Scheduled task for Disc cleanup
- Add .NET Core SDK
