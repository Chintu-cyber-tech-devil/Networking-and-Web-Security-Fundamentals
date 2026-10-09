### Real-World Example: Google IPv4 Address

An IPv4 address identifies a network interface and helps devices communicate over a network. Websites such as Google can be reached using IP addresses.

**Example: Google Public IPv4**

```text
Website: www.google.com
Example IPv4 address: 142.250.183.14
```

*Note: This is an example of a Google IPv4 address. Google's IP addresses can vary depending on location, DNS resolution, and time.*

**IPv4 breakdown:**

```text
142       . 250       . 183       . 14
8 bits      8 bits      8 bits      8 bits

Total = 32 bits
```

Each decimal number is called an **octet**. Each octet represents 8 bits, so IPv4 addresses contain 32 bits in total.

**How to check Google's IPv4 address yourself:**

On Windows, open Command Prompt and run:

```bash
nslookup -type=A google.com
```

Look at the returned IPv4 address or addresses under the DNS answer.

You can also try:

```bash
ping -4 google.com
```

This requests an IPv4 connection attempt; a reply is not guaranteed.

**Cybersecurity connection:** Understanding IP addresses helps security professionals investigate DNS resolution, network traffic, connectivity, and potential network threats.


<img width="690" height="1024" alt="image" src="https://github.com/user-attachments/assets/d17c1468-09ad-4484-89ec-41234187095c" />
