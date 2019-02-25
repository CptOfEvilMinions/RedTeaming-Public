# Windows Deployment

## How to setup WinRM on a Windows machine
1. Start a Powershell prompt as Administrator
1. `Set-ExecutionPolicy Unrestricted`
1. `powershell -NoProfile -ExecutionPolicy Bypass -Command "iex ((new-object net.webclient).DownloadString('https://raw.githubusercontent.com/ansible/ansible/devel/examples/scripts/ConfigureRemotingForAnsible.ps1'))"`
1. `netstat -ano | findstr "LIST"`
    1. If there is a service listening on ports 5985 and 5986 that should be WinRM

## Install/Setup Ansible + PyWinRM
1. MacOS
    1. `brew install python3 python-pip3`
    1. `pip3 install ansible pywinrm`
1. Ubuntu
    1. `apt-get install python3 python-pip3`
    1. `pip3 install ansible pywinrm`
1. Ansible docs
    1. [Ansible installation guide](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
1. Ansible PyWinRM docs
    1. [Windows Remote Management](https://docs.ansible.com/ansible/latest/user_guide/windows_winrm.html)
    1. [WinRM+Ansible](https://digitalist.global/talks/winrmansible/)
    1. [Managing Windows Servers with Ansible](https://www.bloggingforlogging.com/2017/10/12/managing-windows-servers-with-ansible/)

## Download Ansible deployment template
1. `git clone https://github.com/CptOfEvilMinions/RedTeamWindowsDeployment.git`