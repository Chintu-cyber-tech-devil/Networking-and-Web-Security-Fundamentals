Here is the IPv6 version using **Google's website (`www.google.com`)**, without using Google Public DNS.

### Real-World Example: Google IPv6 Address

An IPv6 address identifies a network interface and helps devices communicate over a network. Websites such as Google can be reached using IPv6 addresses when IPv6 connectivity is available.

**Example: Google IPv6**

```text
Website: www.google.com
Example IPv6 address: Obtain it using the command below.
```

*Note: Google's IPv6 addresses can vary depending on location and DNS resolution.*

**IPv6 breakdown:**

IPv6 addresses contain 128 bits, divided into eight groups of 16 bits.

```text
Example format:
2001:0db8:85a3:0000:0000:8a2e:0370:7334

Total = 128 bits
```

Each group contains hexadecimal digits (0–9 and A–F). The `::` symbol can replace consecutive groups of zeros in a compressed address.

**How to check Google's IPv6 address yourself:**

On Windows, open Command Prompt and run:

```cmd
nslookup -type=AAAA www.google.com
```

On Kali Linux, open the terminal and run:

```bash
dig AAAA www.google.com
```

You can test IPv6 connectivity using:

```bash
ping -6 -c 4 www.google.com
```

*Note: If you receive `Network is unreachable`, your system may not have a working IPv6 route.*

**Cybersecurity connection:** Understanding IPv6 helps security professionals analyze network traffic, investigate DNS resolution, identify hosts, and troubleshoot network connectivity and security issues.



<img width="690" height="1024" alt="image" src="https://github.com/user-attachments/assets/4d5c656a-245f-4678-a73b-11eaac423ebf" />










