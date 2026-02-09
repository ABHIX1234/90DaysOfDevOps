# Day 14 – Networking Fundamentals & Hands-on Checks

## Quick Concepts

### OSI vs TCP/IP

- **OSI Model (7 layers):** Physical → Data Link → Network → Transport → Session → Presentation → Application
- **TCP/IP Model (4 layers):** Link → Internet → Transport → Application
- OSI is conceptual (learning/debugging), TCP/IP is practical (real networking).

### Protocol Placement

- **IP** → Network layer (OSI) / Internet layer (TCP/IP)
- **TCP / UDP** → Transport layer
- **HTTP / HTTPS** → Application layer
- **DNS** → Application layer (uses UDP/TCP underneath)

### Real Example

- → Application (HTTP)  
   → Transport (TCP)  
   → Network (IP)

  ***

## Hands-on Checklist

### Identity

```bash
hostname -I
```
