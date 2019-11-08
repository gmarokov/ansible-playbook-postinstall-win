# ansible-win-postinstall
Post Windows installation Ansible script for provisioning dev machine.
Uses WSL to run Ansible over WinRM.

## Installation
1. Enable WSL from the Windows features
2. Install Ubuntu distro from the Store (only supporting Ubuntu for now)
3. Intall Ansible
4. Enable WinRM
5. Add `local 127.0.0.1` to your hosts in `ansible.cfg`

More details about requirement installation here or here.

## Usage
Pull the playbook and execute it. Provide Windows username and password: 
`ansible-pull -U https://github.com/gmarokov/ansible-win-postinstall.git -e ansible-user=your_win_user ansible_password=your_win_user_password 

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

## Contributing
Contributions are more than welcome. Share how you setup your env, the tools you use or the tweaks you make.
