# Introduction

## What?

Virtual network computing, or VNC, is a graphical desktop sharing system that uses the Remote Frame Buffer protocol (RFB) to allow for controlling a server remotely. A VNC server transfers keyboard and mouse events, and displays the remote host’s screen via a network connection (relaying the graphical screen updates back). Servers are best set up as minimal environment, and installing GUI might lead to high hardware utilization. Virtual Network Computing (VNC) is a graphical desktop sharing system  to remotely control another computer. 

## Why?

In our context, only to be used as a fallback when `ssh` fails.

## How?

* [TightVNC](TightVNC.md)
* [TigerVNC](TigerVNC.md)
* [Securing sessions](secure-sessions.md)

## Notes

* VNC is not an encrypted protocol and can be subject to packet sniffing. Sessions can be secured:
  * TightVNC is lightweight and connections will be smooth and stable even on slower internet connections. SSH tunnelling can be used. 
  * TigerVNC supports security schemes such as X509 that combines standard VNC authentication with GNUTLS encryption and server identification. <=
