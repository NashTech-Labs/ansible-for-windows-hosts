An Ansible project template for Windows VM's. 

### How To Setup?

1) Provision your Windows VM by running `scripts/ConfigureRemotingForAnsible.ps1`. This will install WinRM on the Windows VM which is required to accept incoming WinRM connection from Ansible.
2) Your provisioned Windows VM should also accept inbound connections on port 5986 since it's the post used by WinRM to accept `HTTPS` connections.
3) Inside `hosts` file, put the public IP's of your Windows VM's under the `[win_servers]` group (you can name this group anything you want).
4) In the same file, put your Windows VM's password.

### How To Run?

`ansible-playbook playbook.yml -i hosts`

### Features

1) Plug-n-play template to use Ansible for configuration management on Windows VM's.
2) Comes with a sample role to install `Apache`.
