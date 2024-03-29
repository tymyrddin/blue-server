# Introduction

## What?

Server logs contain information that cannot be found anywhere else. For example, server errors and user access records. 

## Why?

Having the ability to review these logs gives the ability to determine what caused an issue on the server.

## How?

* [rsyslogd](rsyslogd.md)
* [Log commands](log-commands.md)
* [Path of a common intruder](intruder-path.md)
* [Logrotate](rotate.md)
* [Centralised logging](centralised.md)

## Notes

* Make sure logs are working properly.
* `syslog` on Debian contains everything except authentication-related messages. 
* Authentication related events can be found in `auth.log`. Use it to investigate failed login attempts, brute-force attacks and other vulnerabilities related to user authorisation mechanisms. RedHat and CentOS based systems use the secure file for tracking all security related messages including authentication failures, `sudo` logins, `ssh` logins and other errors logged by the system security services daemon and is very useful for detecting hacking attempts.
* Additional logs that may give clues are 
  * `faillog` containing information on failed login attempts and can be used to detect attempted security breaches involving username/password hacking and brute-force attacks.
* Normally I am all for distributed and decentralised systems, but for an infrastructure with multiple servers, [centralised logging](centralised.md) saves a lot of time and energy.
* When setting up a machine to act as log server, harden it and only use it to collect logs from other machines on your network. It should not be running anything else.
* Log what is needed to [track the path of a common intruder](intruder-path.md).
* If and when it is all running well, consider setting up for intrusion detection and log correlation.

