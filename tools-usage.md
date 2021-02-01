# Tools usage list

## dnsenum 
[subdomain discovery]
```console
dnsenum --threads 64 --dnsserver 127.0.0.1 -f /usr/share/wordlists/SecLists/Discovery/DNS/subdomains-top1million-110000.txt example.local
```
## wpscan
[bruteforce login]
```console
wpscan --url http://127.0.0.1 -U users.txt -P /usr/share/wordlists/rockyou.txt
```
## wfuzz
[get parameter]
```console
wfuzz -w /usr/share/wordlists/SecLists/Fuzzing/LFI/LFI-gracefulsecurity-linux.txt  --hh 0  'http://127.0.0.1/index.php?FUZZ=test'
```
