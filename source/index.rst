Hardening Linux server
====================================================

.. image:: _static/images/infra.png
  :alt: Overview

----

The below writeups were initially based on debian 9 hosts, and then later on ubuntu 18.04 LTS, and on CentOS 8. Everything
in these writeups will probably also apply to newer versions. If something does not work, check
the documentation for your distro and version for what you are trying to do.

----

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Securing user accounts

   docs/users/README.md
   docs/users/sudo.md
   docs/users/disable-root.md
   docs/users/homes.md
   docs/users/passwords.md
   docs/users/other-reqs.md
   docs/users/lxd.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Audit services

   docs/services/README.md
   docs/services/systemctl.md
   docs/services/netstat.md
   docs/services/nmap.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Firewalls

   docs/firewall/README.md
   docs/firewall/iptables.md
   docs/firewall/ufw.md
   docs/firewall/nftables.md
   docs/firewall/firewalld.md
   docs/firewall/firehol.md
   docs/firewall/pf.md
   docs/firewall/fail2ban.md
   docs/firewall/sshguard.md
   docs/firewall/waf.md
   docs/firewall/port-spoofing.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Encryption technologies

   docs/encryption/README.md
   docs/encryption/gnupg.md
   docs/encryption/files.md
   docs/encryption/openvpn.md
   docs/encryption/strongswan.md
   docs/encryption/ssh.md
   docs/encryption/harden-ssh.md
   docs/encryption/key-management.md
   docs/encryption/jumping.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Virtual network computing (VNC)

   docs/vnc/README.md
   docs/vnc/TigerVNC.md
   docs/vnc/TightVNC.md
   docs/vnc/secure-sessions.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Access control

   docs/access/README.md
   docs/access/dac.md
   docs/access/acl.md
   docs/access/mac.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Public key infrastructure (PKI)

   docs/pki/README.md
   docs/pki/problems.md
   docs/pki/internal-pki.md
   docs/pki/pam.md
   docs/pki/lets-encrypt.md
   docs/pki/tls-ssl.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Logfiles

   docs/logfiles/README.md
   docs/logfiles/rsyslogd.md
   docs/logfiles/log-commands
   docs/logfiles/intruder-path.md
   docs/logfiles/rotate.md
   docs/logfiles/centralised.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Disasters

   docs/disasters/README.md
   docs/disasters/prevention.md
   docs/disasters/git.md
   docs/disasters/backup.md
   docs/disasters/brm.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Guards! Guards!

   docs/ids/README.md
   docs/ids/samhain.md
   docs/ids/*

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Troubleshooting

   docs/trouble/README.md
   docs/trouble/*

.. toctree::
   :caption: Links

   Blue Team <https://blue.tymyrddin.dev/>

----

.. image:: _static/images/linux-hardening-book.png
  :alt: Useful books

Wishlist: server configurations for a separate authentication server, log server, and DNS server, and a
Maltrail firewall implemented on the Bastion jumpserver.

