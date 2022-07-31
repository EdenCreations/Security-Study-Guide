# NMAP

Nmap can be used to scan web ports. This is particularly useful because they can be used to spot vulnerabilities.

**TCP Ports**

Port 80 -> Standard port address for web servers that utilize the HTTP Protocol.
Port 21 -> FTP
Port 22 -> SSH
Port 25  -> [[SMTP]] (sending Email)
Port 53 -> DNS (Domain Name Service)
Port 110 - POP3 (Email inbox)
Port 123 -> NTP (Network Time Protocol)
Port 443 -> HTTPS (Secure Web-Server)
Port 465 -> SMTPS (send secure email)
Port 631 -> CUPS (print server)
Port 993 -> IMAPS (Secure email inbox)
Port 995 -> POP3 (Secure email inbox)


"Open" high numbered ports are usually associated with transient services. An example would be the FTP protocol where high numbered ports come and go with each file transfer.

Linux firewalls can be configured to block traffic on a particular port.

For example: Firewalls can be set to block Port 80 but then users won't be able to load any website. Firewall rules can be used in tandem to allow some ports, but block others. Thus used in conjunction with other network security tools and software, one can scan traffic on a particular port and watch for suspicious traffic.

### Best Practices
It's best practice to only use Nmap port scanning on servers you own or have permission to scan because port-scanning is often seen as an aggressive method or a prelude to a cyber attack. It's also bad practice to tie up server resources to run repeated scans on the same target.