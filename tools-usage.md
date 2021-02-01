# Tools usage list

## dnsenum 
### subdomain discovery
```console
dnsenum --threads 64 --dnsserver 127.0.0.1 -f /usr/share/wordlists/SecLists/Discovery/DNS/subdomains-top1million-110000.txt example.local
```
## wpscan, brute force
### bruteforce login
```console
wpscan --url http://127.0.0.1 -U users.txt -P /usr/share/wordlists/rockyou.txt
```
