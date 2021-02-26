# Tools usage list
## gobuster
[directory scan]
```console
gobuster dir -k -u http://127.0.0.1/ -w list.txt -x .php,.txt,.bak,.html
```
## dnsenum 
[subdomain discovery]
```console
dnsenum --threads 64 --dnsserver 127.0.0.1 -f subdomains-top1million-110000.txt example.local
```
## wpscan
[bruteforce login]
```console
wpscan --url http://127.0.0.1 -U users.txt -P /usr/share/wordlists/rockyou.txt
```
[enumerate users]
```console
wpscan --url http://127.0.0.1 --enumerate u
```
## wfuzz
[get parameter]
```console
wfuzz -w lfi-list.txt  --hh 0  'http://127.0.0.1/index.php?FUZZ=test'
```
## JtR
[hash crack]
```console
john hash --wordlist=/usr/share/wordlists/rockyou.txt
```
## Hydra 
[post login brute force]
```console
hydra -l admin -P /usr/share/wordlists/rockyou.txt 127.0.0.1 http-post-form "/login.php:username=^USER^&password=^PASS^&Login=Login:Login Failed"
```
