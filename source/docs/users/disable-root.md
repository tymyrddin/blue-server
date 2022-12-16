# Disabling root access

## Disabling the root login shell

When creating a virtual private server on a cloud service (Rackspace, DigitalOcean, Vultr), the cloud service will
have you log in to that virtual machine as the root user. (Even with Ubuntu).

The first thing that you will want to do is to create a normal user account and give it full sudo privileges. Then, 
log out of the root account and log back in with the normal user account. Then disable the root account:

    sudo passwd -l root

## Disabling root SSH login

## Disabling root using PAM