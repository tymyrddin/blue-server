Linux server mitigations
====================================================

.. image:: _static/images/infra.png
  :alt: Overview

Version 0.1: Notes on setting up a base linux server for building a secure infrastructure with separated servers.
The below configurations were for a debian 9, and need to be updated, an authentication server and DNS server added,
and a Maltrail firewall implemented on the Bastion jumpserver. A work in progress ...

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: SSH

   docs/ssh/README.md
   docs/ssh/install-ssh.md
   docs/ssh/harden-ssh.md
   docs/ssh/key-management.md
   docs/ssh/jumping.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: VPN

   docs/vpn/README.md
   docs/vpn/*

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: VNC

   docs/vnc/README.md
   docs/vnc/TigerVNC.md
   docs/vnc/TightVNC.md
   docs/vnc/secure-sessions.md

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
   docs/logfiles/intruder-path.md
   docs/logfiles/rotate.md
   docs/logfiles/centralised.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Backup

   docs/backups/README.md
   docs/backups/*

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Firewall

   docs/firewall/README.md
   docs/firewall/iptables.md
   docs/firewall/nftables.md
   docs/firewall/firewalld.md
   docs/firewall/firehol.md
   docs/firewall/ufw.md
   docs/firewall/pf.md
   docs/firewall/fail2ban.md
   docs/firewall/sshguard.md
   docs/firewall/waf.md
   docs/firewall/port-spoofing.md

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
   :caption: All mitigations

   Overview <https://tymyrddin.github.io/mitigations/>
