# Introduction

## What?

Protect data at rest and data in transit.

## Why?

* Confidentiality: This ensures that only people who are authorised to see the data can see it.
* Integrity: This ensures that original data has not been altered by unauthorised people.
* Availability: This ensures that sensitive data is always available, and can not be deleted by unauthorised people.

## How?

* [GNU Privacy Guard](gnupg.md)
* [OpenVPN](openvpn.md)
* [strongSwan](strongswan.md)
* [Installing SSH](ssh.md)
* [Harden ssh server](harden-ssh.md)
* [Key management](key-management.md)
* [Jumping hosts](jumping.md)


## Notes

* Using a VPN is a way to map out a private network that only the servers can see. Communication will be fully private and secure. Other applications can be configured to pass their traffic over the virtual interface that the VPN software exposes. This way, only services that are meant to be used by clients on the public internet need to be exposed on the public network.
* Install and configure ssh keys and make your servers require them to minimise the risk posed by adversaries.  
* Harden the ssh server (also harden default service settings in web server and other services)
* Do not leave passphrase empty - An adversary who gets hold of your private key can otherwise connect to the hosts where you put you public key.
* Use a separate key per client you ssh from to the same server. If one key is compromised the damage is more limited and easier to clean up.
* Limit the number of clients you ssh from. If a client is compromised an adversary has your key, they can install a binary to get your passwords/passphrases.
* If any, disable the ssh-server on the client machine you ssh from. Limit the attack surface.
* Don't make jump host chains too long. If one client in the chain is compromised, an adversary can use that to compromise the rest of the clients down the chain. 
* Don't use Agent Forwarding. While being connected to the first host, anyone with sufficient permission on the first host will be able to use that socket to connect to and use that local ssh-agent. A rogue root or evil admin with root access can eavesdrop on the ongoing session and impersonate the user for authentication to other servers during the time that user is connected to that server. Instead, use ProxyJump (it uses E2EE) or, if that is not possible, use ProxyCommand.
* In some countries, proving that you connected to a particular server is enough to be prosecuted, but SSH doesn't provide a native way to obfuscate to whom it connects. For that, SSH with Tor can be used.
* Don't ignore authentication errors. This warning is protecting you. The remote host key is different than the client knows. Make sure the key really did change. An adversary may be spoofing the host and continuing may give the adversary the information they seek to attack your server. Another reason to not use passwords. 

