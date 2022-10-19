# Empty Server Project

## A simple linux server to practice bash and command line skills

### Info/Prerequisites:
Use this to generate an empty server where you can spin up and tear down as needed.

Vagrant and Virtual Box installation is required

If on mac and have homebrew installed, try doing:

```bash
vagrant --version
```

If the command is not found, then perform:

```bash
brew install --cask vagrant
```

### How to start the server

In the directory where the 'Vagrantfile' is located, run this command:

```bash
vagrant up
```

If it completes successfully, you can log in by performing the following:

```bash
vagrant ssh
```

To stop the running virtual machine, perform the following:

```bash
vagrant halt
```

To destroy the virtual machine and be able to start from scratch:

```bash
vagrant destroy
```
or

```bash
vagrant destroy; vagrant up
```

Check ip-address to see if it matches what is in the vagrant file we explicitly defined

```bash
ifconfig
```

Check the space available

```bash
df -h
```

check general server information

```bash
uname -a
```

download tools

```bash
yum install <tool-name-here>
```

Have fun!


## Common Issues and how to troubleshoot

### "Progress: 90%There was an error while executing 'VBoxManage', a CLI used by Vagrant for controlling VirtualBox. The command and stderr is shown below."

If this occurs, your virtual box may be having issues creating a folder for a new machine. Try opening VirtualBox, then under File > Preferences, update the file path to something that is available

### "The IP address configured for the host-only network is not within the allowed ranges. Please update the address used to be within the allowed ranges and run the command again."

Seems to be an issue with some Ubuntu versions.

A solution to this could be to create a new file /etc/vbox/networks.conf on macOS with the contents:

```bash
mkdir /etc/vbox/
sudo vi networks.conf
```

And enter the following

```bash
* 10.0.0.0/8 192.168.0.0/16
* 2001::/64
```

Be sure to include the asterisks '*'. The issue should hopefully be gone.


