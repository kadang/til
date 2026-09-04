# Creating a bootable USB drive

To create a bootable USB drive, the [Arch Linux wiki]() has a number of suggestions.
For me, only one of them worked (on EndeavourOS), and it only worked when run as `root`:

```
sudo dd bs=4M if=path/to/<iso-file>.iso of=/dev/sda conv=fsync oflag=direct status=progress
```

Make sure that `of` points to the right device (*not* a partition on the device), and that it isn't mounted.
Check with `lsblk`.
