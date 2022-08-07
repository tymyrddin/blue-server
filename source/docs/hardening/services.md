# Restrict services

Run only what you need. 

## Check

What kind of services are running on the system:

    # ps ax

Processes accepting connection (ports):

    # netstat -lp

## Typical candidates for removal

Most likely candidates for removal:

* `smbd` and `nmbd` indicates a Samba Process. Do you really need to export smb share on windows or other machine?
* `telnet` for bidirectional interactive text-oriented communication over internet or local area network? 
* `rlogin` to log in to another host over network?
* `rexec` to execute shell commands on a remote computer.
* `ftp` to transfer files from one host to another host over Internet?
* `automount` to mount different file systems automatically to bring up network file system? 
* `named` to run NameServer (DNS)? 
* `lpd` to print to the server. 
* `inetd`? If you are running standalone applications like `ssh` which uses other standalone application like `mysql`, `Apache`, etc. then you don’t need inetd.
* `portmap`, an Open Network Computing Remote Procedure Call (ONC RPC) which uses `rpc.portmap` and `rpcbind`. If these processes are running, you are running NFS server. Really? NFS server is running unnoticed?

## Stop and disable

To stop a service, then prevent it from restarting at reboot:

    sudo systemctl stop <service>
    sudo systemctl disable <service>

Example:

    sudo systemctl stop smbd
    sudo systemctl disable smbd