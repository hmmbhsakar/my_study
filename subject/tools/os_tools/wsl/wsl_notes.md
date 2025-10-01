# Notes
## Default Terminal
I found that Zutty is the default terminal emulator in case of Ubuntu being installed in WSL. Following command was helpful to check the same:
`sudo update-alternatives --config x-terminal-emulator`

# How To

## Mount Google Drive (Virtual Drive) into WSL

To Mount Google Drive (virtual Drive) in windows that is shown after installation of google drive local disk in computer. First create a directory in the linux distro to mount to and then mount like any other drive mounting. Creating a mount destination directory (`sudo mkdir /mnt/d`, replacing d with whatever drive letter you'd like to use) and then using the drvfs file system interop plugin, with the command:

```bash  
sudo mkdir [/mnt/any_drive_name]   # First run this to create a directory to mount  
sudo mount -t drvfs [window_drive_to_mount]:D: [/mnt/newly_created_directory_using_above_line_code] # Now enter this line code by replacing window drive to mount name and created dir in previous line  
```

## Automating Drive Mount with

You can use the /etc/wsl.conf file inside your Ubuntu distribution to automate the mounting process. Specifically, you’ll want to:

1. Enable mountFsTab: This allows WSL to process /etc/fstab on startup.  
2. Add an entry in /etc/fstab for window drive `[drive_letter]:`. Example `G:`

Step-by-step setup:

1. Edit `/etc/wsl.conf`:

   ```ini
   [automount]  
   enabled = true  
   mountFsTab = true 
   ```

2. Create or edit /etc/fstab:
Add this line to mount window Drive automatically:

   ```bash
   [drive_letter]: /mnt/[distro_mount_destination] drvfs defaults 0 0
   ```

   Example:

   ```bash
   G: /mnt/g drvfs defautls 0 0
   ```

3. Restrat WSL:
   Run this is in Powershell to apply changes:

   ```Powershell
   wsl --shtudown
   ```

This setup ensures that every time WSL starts, it will automatically mount Drive to `/mnt/[distro_mount_destination]` without needing to manually run the sudo mount command.
