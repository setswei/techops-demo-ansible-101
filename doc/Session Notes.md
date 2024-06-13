## Introduction
This document has been written to provide a 101 introduction course to [[ansible]] for [[Idea 11]] TechOps Seniors.

## Course Introduction 
- What is Ansible
	- Ansible essentially is a Configuration Management Tool for Servers
	- Call out the difference between ansible vs products like terraform/Cloudformation.
	- Over time ansible has evolved to do more then this though due to a large community that has leveraged ansible to fill automation needs where other products were lacking.
- Ansible was released in 2012 in the time where there were already other products that were dominating the market (this products were Chef, Puppet and CF Engine)
- Products like Chef and Puppet required you to learn complicated programming languages Ruby or Puppets Declarative Language.
- Ansible offered a simpler approach to configuration management by being an agent-less solution that utilises YAML (YAML is a human readable data serialisation language, otherwise called Yet another markdown language.). 
- Due to it simplistic approach and much easier learning curve its adoption was huge and extremely quick, Redhat came along and saw a opportunity and brought it out in 2015.

## Components
These are the core components of ansible.
- **Control Node**: This is where ansible is being executed from.
- **Managed Node**: Server or devices that your managing with ansible.
- **Inventory**: A list of managed nodes provided by one or more inventory sources.
- **Playbooks**: Contains Plays (which are the basic unit of a ansible execution)
	- **Plays:** Are the main context for ansible execution plays map managed nodes to tasks.
	- **Roles:** A limited distribution of reusable ansible content that can be used inside a play.
	- **Tasks**: The definition of an action to be applied to the managed host.
	- **Handlers:** A special form of task that only executes when notified by a previous task which resulted in a `changed` status
- **Modules:** Code or binaries that ansible copies to and executes on each managed node.
- **Plug-ins**: Pieces of code that expand ansible’s core capabilities.
- **Collections:** A format in which Ansible content is distributed that can contain multiple playbooks, roles and modules.

## Ansible Connection Methods
Ansible was natively built to connect using OpenSSH. This 101 Course/Demo will only be going over SSH.  Ansible does however support other connection types, some of these are listed below.
- WinRM (HTTP/HTTPS)
- Native HTTP/HTTPS.
- Other Customised Options provided 3rd party plug-ins.

## How to Install Ansible

>[!Warning]
> Ansible cannot be installed within a native windows environment. If you run windows you are best to utilise Windows Subsystem for Linux (WSL).

Ansible can be installed using packager managers like `apt` or `yum` . MacOS can even use `homebrew` . However my preferred method is using Python’s Package Manager `pip`.

```Bash
pip install ansible
```

## Demo

* Show example repository
	* Explain the Configuration File
	* Explain the inventory file
	* Explain the playbook.yaml

* Do a Connectivity Test using Ansible Ping `ansible ping -i inventory WebServers`
* Run Playbook against Single Server
* Show HTTP can be hit
* Run Playbook against WebServers `ansible-playbook playbook.yml -i inventory -K`
* Talk to extending the playbook to use roles and maintain configuration
* Demo other use case example the Mac Dev Playbook



