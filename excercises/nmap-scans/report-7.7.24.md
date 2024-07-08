
# Nmap 7.94SVN scan initiated Sun Jul  7 14:09:34 2024 as: nmap -sV -p0-65535 -oN /home/kali/Desktop/nmap_scan_results.txt 192.168.2.1/24

## Nmap scan report for 192.168.2.1
- **Host Status:** Up (0.0013s latency)
- **Not shown:** 65533 filtered tcp ports (no-response)
- **Open Ports:**
  - 53/tcp: open domain (Unbound)
  - 80/tcp: open http (nginx)
  - 443/tcp: open ssl/http (nginx)

## Nmap scan report for DESKTOP-6NM36N8.home.arpa (192.168.2.2)
- **Host Status:** Up (0.0016s latency)
- **Not shown:** 65524 closed tcp ports (conn-refused)
- **Open Ports:**
  - 0/tcp: filtered unknown
  - 135/tcp: open msrpc (Microsoft Windows RPC)
  - 139/tcp: open netbios-ssn (Microsoft Windows netbios-ssn)
  - 445/tcp: open microsoft-ds?
  - 5040/tcp: open unknown
  - 49664/tcp: open msrpc (Microsoft Windows RPC)
  - 49665/tcp: open msrpc (Microsoft Windows RPC)
  - 49666/tcp: open msrpc (Microsoft Windows RPC)
  - 49667/tcp: open msrpc (Microsoft Windows RPC)
  - 49668/tcp: open msrpc (Microsoft Windows RPC)
  - 49669/tcp: open msrpc (Microsoft Windows RPC)
  - 49670/tcp: open msrpc (Microsoft Windows RPC)

- **Service Info:**
  - OS: Windows
  - CPE: cpe:/o:microsoft:windows

## Nmap scan report for 192.168.2.3
- **Host Status:** Up (0.0028s latency)
- **Not shown:** 65505 closed tcp ports (conn-refused)
- **Open Ports:**
  - 0/tcp: filtered unknown
  - 21/tcp: open ftp (vsftpd 2.3.4)
  - 22/tcp: open ssh (OpenSSH 4.7p1 Debian 8ubuntu1 (protocol 2.0))
  - 23/tcp: open telnet (Linux telnetd)
  - 25/tcp: open smtp (Postfix smtpd)
  - 53/tcp: open domain (ISC BIND 9.4.2)
  - 80/tcp: open http (Apache httpd 2.2.8 ((Ubuntu) DAV/2))
  - 111/tcp: open rpcbind 2 (RPC #100000)
  - 139/tcp: open netbios-ssn (Samba smbd 3.X - 4.X (workgroup: WORKGROUP))
  - 445/tcp: open netbios-ssn (Samba smbd 3.X - 4.X (workgroup: WORKGROUP))
  - 512/tcp: open exec (netkit-rsh rexecd)
  - 513/tcp: open login?
  - 514/tcp: open shell (Netkit rshd)
  - 1099/tcp: open java-rmi (GNU Classpath grmiregistry)
  - 1524/tcp: open bindshell (Metasploitable root shell)
  - 2049/tcp: open nfs 2-4 (RPC #100003)
  - 2121/tcp: open ccproxy-ftp?
  - 3306/tcp: open mysql (MySQL 5.0.51a-3ubuntu5)
  - 3632/tcp: open distccd (distccd v1 ((GNU) 4.2.4 (Ubuntu 4.2.4-1ubuntu4)))
  - 5432/tcp: open postgresql (PostgreSQL DB 8.3.0 - 8.3.7)
  - 5900/tcp: open vnc (VNC (protocol 3.3))
  - 6000/tcp: open X11 (access denied)
  - 6667/tcp: open irc (UnrealIRCd)
  - 6697/tcp: open irc (UnrealIRCd)
  - 8009/tcp: open ajp13 (Apache Jserv (Protocol v1.3))
  - 8180/tcp: open http (Apache Tomcat/Coyote JSP engine 1.1)
  - 8787/tcp: open drb (Ruby DRb RMI (Ruby 1.8; path /usr/lib/ruby/1.8/drb))
  - 35861/tcp: open nlockmgr 1-4 (RPC #100021)
  - 40352/tcp: open mountd 1-3 (RPC #100005)
  - 40823/tcp: open java-rmi (GNU Classpath grmiregistry)
  - 49118/tcp: open status 1 (RPC #100024)

- **Service Info:**
  - Hosts: metasploitable.localdomain, irc.Metasploitable.LAN
  - OSs: Unix, Linux
  - CPE: cpe:/o:linux:linux_kernel

**Service detection performed. Please report any incorrect results at [Nmap](https://nmap.org/submit/).**

# Nmap done at Sun Jul  7 14:15:12 2024 -- 256 IP addresses (3 hosts up) scanned in 337.78 seconds
