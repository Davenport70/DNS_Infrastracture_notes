# DNS Route 53

## What is DNS

The Domain Name System (or DNS) converts human readable domain names (like: www.google.com) into Internet Protocol (IP) addresses (like: 173.194.39.78).

Computers can only communicate using series of numbers, so DNS was developed as a sort of “phone book” that translates the domain you enter in your browser into a computer readable IP.

## How does it work

Nameservers store DNS records which are the actual file that says “this domain” maps to “this IP address”.

These nameservers are called the root nameservers and instead of storing every domain ever, they store the locations of the TLD (top level domains).

TLD’s are the two or three character like .com that end a domain name. Each TLD has their own set of nameservers that store the information that says who is authoritative for storing the DNS records for that domain.

## What are A records, MX records and CNAME records

A - specifies IP addresses corresponding to your domain and its subdomains;

MX - specifies where the emails for your domain should be delivered;

CNAME - specifies redirects from your domain's subdomains to other domains / subdomains;

## What is route 53

**Three main purposes**

- Domain registration—Amazon Route 53 lets you register domain names, such as
example.com.
- DNS service—Amazon Route 53 translates friendly domain names like
www.example.com into IP addresses like 192.0.2.1. Amazon Route 53 responds to DNS
queries using a global network of authoritative DNS servers, which reduces latency. To comply with DNS standards, responses sent over User Datagram Protocol (UDP) are limited to 512 bytes in size. Responses exceeding 512 bytes are truncated, and the resolver must re-issue the request over TCP.
- Health checking—Amazon Route 53 sends automated requests over the Internet to
your application to verify that it’ s reachable, available, and functional..

**Author**

**Zack Davenport** - *Junior DevOps Engineer* - Davenport70
