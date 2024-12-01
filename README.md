Configured and deployed an NFS (Network File System) server and client setup to enable seamless file sharing across a network. The NFS server was configured on a dedicated machine (IP: 172.31.44.132) by installing the necessary NFS server packages using the sudo apt install nfs-kernel-server command. The shared directory was defined in the /etc/exports file with specific permissions, allowing read and write access for a specified client IP (172.31.46.255). Proper directory structure and permissions were created using commands like mkdir, chown, and chmod to ensure secure access and data integrity.

To ensure continuous availability, the NFS server was started and enabled to run on system boot using systemctl. Additionally, firewall rules were configured to allow access to the NFS server from the client IP. On the client side, the nfs-common package was installed, and a mount point was created to mount the shared directory. The NFS share was mounted using the mount command and verified with df -h to ensure proper connectivity. Furthermore, to ensure automatic mounting at boot, the /etc/fstab file was configured to include the NFS share, making the setup persistent across reboots.

A key component of the setup was verifying file creation on both the server and client side. Files were created on the shared directory from both ends using commands like touch and validated with ls -l to ensure proper file access and synchronization. The client machine was tested for automatic mounting by rebooting or running the mount -a command to confirm that the shared directory was correctly mounted and accessible.

This project demonstrated proficiency in configuring network-based file sharing, ensuring secure and reliable access to shared resources, and automating mount processes for smooth operation. It also highlighted the ability to manage both server and client-side configurations to ensure efficient and secure file sharing over a network.
