---
date: 2023-05-17 
categories:
  - Devlog
tags:
  - nginx
  - learning
---

# Nginx - Troubleshooting Errors
#### When Uninstalling and Reinstalling it on my local machine

Recently, I ran into a tricky issue while trying to uninstall **Nginx** from my BunsenLabs system. Initially, I just wanted a fresh start, but the process ended up being more complicated than I expected, and finding the right solution took quite a bit of time.

Here’s what happened… <!-- more -->

## The Problem's Root

In a rush to clean up, I went straight to deleting the configuration directory for `Nginx` in `/etc/nginx` without properly uninstalling the `Nginx` package from the system. This meant that when I did go to remove the package later and reinstall it, the install process failed. Checking inside the `Nginx` config directory showed that all the usual folders under `/etc/nginx` were re-created but were completely empty.

This led me to a bit of a dead end, so I turned to StackOverflow, hoping to find a fix. I found some suggestions recommending a “full-fledged” uninstall—essentially removing every trace of `Nginx` to start from scratch. However, I couldn’t remember the exact command sequence, and my browser history with the links I’d saved was deleted, adding to my frustration.

---

## Steps to Completely Uninstall and Reinstall Nginx on BunsenLabs

After a fair bit of searching, I finally found the complete steps to resolve the issue. If anyone else runs into a similar problem, here’s what worked for me:

 **Fully Uninstall the Nginx Package**

   In your terminal, run this command to remove `Nginx` along with any configuration files in directories like `/etc/nginx`.

   ```bash linenums="1"
   sudo apt purge --auto-remove nginx nginx-common
   ```

   This command ensures all configuration files are removed, so we don’t have to hunt them down manually.

 **Clean Up Nginx Cache and Data**

   To make sure every trace of `Nginx—cache`, `logs`, or otherwise—is removed from the system, use the following commands:

   ```bash linenums="1"
   sudo apt clean
   sudo rm -rf /etc/nginx
   sudo rm -rf /var/log/nginx
   sudo rm -rf /var/lib/nginx
   ```

   This thoroughly cleans up any leftover `Nginx` files from the system.

 **Reinstall Nginx**

   Now that the old install is completely removed, it’s time to reinstall `Nginx` from scratch. Update the package list and install `Nginx` as usual:

   ```bash linenums="1"
   sudo apt update
   sudo apt install nginx
   ```

   This time, once the installation is complete, `Nginx` should create all necessary directories and default configuration files under `/etc/nginx` without any issues.

---

This taught  me ;) to be a little more cautious about deleting directories, especially critical ones that contain application configurations like `Nginx`. If you ever need a full reset or reinstall, it’s best to fully uninstall all related components to avoid unexpected headaches when you try to reinstall.

Hopefully, this story helps anyone out there facing a similar issue. Feel free to follow these steps if you’re looking to completely reinstall `Nginx` on your system.
