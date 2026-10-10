### IPv6 — 128-bit Address (8 Groups)

#### Real-World Example: Google Public DNS IPv6

IPv6 (Internet Protocol Version 6) is a network-layer protocol designed to provide a much larger address space than IPv4.

**Example:**

```text
Website: dns.google
IPv6 Address: 2001:4860:4860::8888
```

#### IPv6 Address Breakdown

```text
2001:4860:4860:0000:0000:0000:0000:8888
```

* **Total size:** 128 bits
* **Number of groups:** 8
* **Each group:** 16 bits
* **Number system:** Hexadecimal (0–9 and A–F)
* **Separator:** Colon (`:`)

#### How to Check Google's IPv6 Address

**Windows Command Prompt:**

```bash
nslookup -type=AAAA dns.google
```

**Kali Linux:**

```bash
dig AAAA dns.google
```

**Cybersecurity Connection:** IPv6 knowledge helps security professionals analyze network traffic, investigate DNS records, and identify hosts on IPv6 networks.












