# change-linux-hostname
This guide provides step-by-step instructions to change a system's hostname from an IP address to a custom name. It covers updating the hostname using hostnamectl, modifying the /etc/hosts file, and rebooting the system for changes to take effect. The instructions are formatted for GitHub documentation, making them easy to read and follow.
# Changing Hostname from IP to Name

Follow these steps to change your system hostname from an IP address to a custom name.

## 1. Change the Hostname  
To update the system hostname, use the `hostnamectl` command:  

```sh
hostnamectl set-hostname <name>
```
This command sets the new hostname to `<name>`.

## 2. Update the `/etc/hosts` File  
You need to modify the `/etc/hosts` file to reflect the new hostname.  

### Steps:  
1. Open the file in a text editor:  

   ```sh
   sudo nano /etc/hosts
   ```
2. Locate the following line:  

   ```sh
   127.0.0.1   localhost
   ```
3. Modify it to include the new hostname:  

   ```sh
   127.0.0.1   localhost name
   ```
4. Save and exit the editor (`CTRL + X`, then `Y`, then `Enter`).

## 3. Reboot the System  
For the changes to take effect, reboot the system using:  

```sh
sudo reboot
```
Once the system reboots, the hostname will be updated to `<name>`.
