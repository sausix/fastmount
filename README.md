# fastmount
# by Adrian Sausenthaler

Do you mount a lot of filesystems in the terminal?
Is /mnt already in use for your next mount?
Just wanna have a short look into the root folder of a block device to identify it?

Try fastmount.

It creates a unique directory, mounts into it and starts a new bash for your operations.
Just exit the session with Ctrl+D and the device gets unmounted automatically.


General usage:
	fastmount <block device> [mountoptions]

Mounts the filesystem in /dev/sda1:
	fastmount /dev/sda1

Mounts the subvolume '@' of a btrfs filesystem read only:
	fastmount /dev/sda1 subvol=@,ro
