# Ports and Services

## 1. What Is a Port?

A port is a logical communication endpoint used by applications to send and receive network data.

- IP address identifies a device or network interface.
- Port number helps identify an application service.
- Port numbers range from `0` to `65535`.

Example: `192.168.1.10:443`

Here, `192.168.1.10` is the IP address, and `443` is the port number.

## 2. What Is a Service?

A service is a program that provides a function over a network, such as web hosting, remote login, or file sharing.

Examples:
- HTTP — Web communication
- SSH — Secure remote access
- DNS — Domain name resolution
- FTP — File transfer

## 3. Common Ports and Services

| Port  | Protocol| Service        | Purpose 
|---    |---      |---             |---
| 20/21 | TCP     | FTP            | File transfer 
| 22    | TCP     | SSH            | Secure remote access 
| 23    | TCP     | Telnet         | Remote terminal access 
| 25    | TCP     | SMTP           | Email transfer 
| 53    | UDP/TCP | DNS            | Domain name resolution 
| 67/68 | UDP     | DHCP           | Automatic IP configuration 
| 80    | TCP     | HTTP           | Web communication 
| 110   | TCP     | POP3           | Email retrieval 
| 123   | UDP     | NTP            | Time synchronization 
| 143   | TCP     | IMAP           | Email access 
| 443   | TCP/UDP | HTTPS / HTTP/3 | Secure web communication 
| 445   | TCP     | SMB            | File sharing 
| 3306  | TCP     | MySQL          | Database access 
| 3389  | TCP/UDP | RDP            | Remote desktop 
| 5432  | TCP     | PostgreSQL     | Database access 
| 8080  | TCP     | HTTP alternate | Web applications 
| 27017 | TCP     | MongoDB        | Database access 

Note: Ports shown are common defaults. Services can use different ports depending on configuration.

## 4. Port Number Ranges

| Range       | Category 
|---          |---
| 0–1023      | Well-known ports 
| 1024–49151  | Registered ports 
| 49152–65535 | Dynamic or private ports 

## 5. Why Are Ports Important in Cybersecurity?

- Identify exposed network services.
- Detect unnecessary open ports.
- Help investigate suspicious connections.
- Support firewall configuration.
- Help identify potentially vulnerable services.

## 6. Common Port Security Risks

- Telnet sends data without encryption.
- Exposed databases can be attacked.
- Outdated services may contain vulnerabilities.
- Unnecessary open ports increase the attack surface.
- Weak remote-access credentials can allow unauthorized access.

## 7. Port Security Best Practices

- Close unnecessary ports.
- Use encrypted protocols such as SSH instead of Telnet.
- Restrict database access to trusted systems.
- Keep services updated.
- Use firewalls and strong authentication.
- Scan only systems you own or have permission to test.



# Nmap Scanning

## 1. What Is Nmap?

Nmap stands for Network Mapper.

Nmap is a network discovery and security auditing tool used to identify hosts, open ports, and network services.

## 2. Why Is Nmap Used?

- Discover devices on a network.
- Identify open ports.
- Detect running services.
- Attempt service-version detection.
- Help administrators audit network security.
- Support authorized penetration-testing labs.

## 3. Basic Nmap Commands

### 1. Basic Scan

```bash
nmap 192.168.1.10
```

Scans common TCP ports on the target.

### 2. Scan Specific Ports

```bash
nmap -p 22,80,443 192.168.1.10
```

Scans ports 22, 80, and 443.

### 3. Scan All TCP Ports

```bash
nmap -p- 192.168.1.10
```

Scans TCP ports 1–65535.

### 4. Detect Service Versions

```bash
nmap -sV 192.168.1.10
```

Attempts to identify the services and versions running on discovered ports.

### 5. SYN Scan

```bash
sudo nmap -sS 192.168.1.10
```

Uses TCP SYN probes to scan ports where supported.

### 6. UDP Scan

```bash
sudo nmap -sU --top-ports 100 192.168.1.10
```

Scans a selection of common UDP ports.

### 7. Scan a Local Subnet

```bash
nmap 192.168.1.0/24
```

Discovers hosts and scans common TCP ports across the specified subnet.

Replace the example addresses with targets in your own authorized lab.

## 4. Understanding Nmap Results

| State    | Meaning 
|---       |---
| Open     |  An application is listening on the port. 
| Closed   | The host responds, but no application is listening on the port. 
| Filtered | Filtering or missing responses prevents Nmap from determining whether the port is open. 

## 5. Nmap and Cybersecurity

Nmap helps security professionals understand which services are exposed and where further defensive investigation may be necessary.

An open port does not automatically mean a vulnerability exists. The service, its configuration, and its software version must also be evaluated.

## 6. Responsible Scanning

- Scan only systems you own or have explicit permission to test.
- Avoid disrupting production systems.
- Use a virtual machine or isolated lab for practice.
- Do not assume a scan result proves that a system is secure.

## 7. Official Resources

- Nmap website: https://nmap.org/
- Nmap reference guide: https://nmap.org/book/man.html


