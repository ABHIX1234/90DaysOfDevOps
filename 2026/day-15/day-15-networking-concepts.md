# Day 15 – Networking Concepts: DNS, IP, Subnets & Ports

## Task 1: DNS – How Names Become IPs

### 1. What happens when you type `google.com` in a browser?

When we enter `google.com`, the browser first checks local cache. If not found, it queries a DNS resolver, which asks root servers, then TLD servers (.com), and finally Google’s authoritative DNS server. The DNS server returns Google’s IP address, and the browser connects to that IP.

### 2. DNS Record Types

- **A** – Maps a domain name to an IPv4 address
- **AAAA** – Maps a domain name to an IPv6 address
- **CNAME** – Alias of one domain name to another
- **MX** – Mail server responsible for receiving emails
- **NS** – Name servers for the domain

### 3. `dig google.com` Output

```bash
;; ANSWER SECTION:
google.com.    300    IN    A    142.250.183.14
```

🔹 What is an IPv4 address?

An IPv4 address is a 32-bit numerical identifier used to uniquely identify devices on a network.
It is written in dotted-decimal format (e.g., 192.168.1.10).

🔹 Public vs Private IP Addresses
Type Description Example
Public IP Accessible over the internet 8.8.8.8
Private IP Used within local networks 192.168.1.10
