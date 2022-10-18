# Simple Projects

## We will start developing projects that allow for virtual environments to run special tools for development and testing

Please add more content!

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


