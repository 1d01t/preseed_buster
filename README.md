# preseed_buster


this is a preseed file, to autoinstall debian buster on a machine


Prepare
------------

  - Place this file at a reachable place for http or sftp server
  - Enter the name, the new machine should get to your dhcpd server
  - you need a crypted root pwd, so install whois on a machine and execute: mkpasswd -m sha-512
  - set the previous generated password at line: 124
  - place your public ssh-key at a reachable place
  - set the previous path at line: 448

Modify the project to fit your needs
------------

  - locales and keyboard is set do de_DE
  - the hostname is gotten from dhcp server. If not set, it takes "debian" as hostname
  - time is set to UTC
  - it installes into an lvm
  - ssh-server starts at boot
  - tasksel gets installed
  - root login gets permitted with ssh-key only

run the setup
------------

  - start debian-buster.iso
  - go to "Advanced settings"
  - go to "Automated install"
  - type in the path where the machine can reach the file
