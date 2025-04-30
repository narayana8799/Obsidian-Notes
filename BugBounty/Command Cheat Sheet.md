Fuzzing
--
### ffuf

```
Directory Fuzzing => ffuf -w /path/to/wordlist.txt:FUZZ -u https://url/FUZZ

VHost Fuzzing => ffuf -w /path/to/wordlist.txt:FUZZ -u http://academy.htb:PORT/ -H 'Host: FUZZ.academy.htb'

Sub-Domain Fuzzing => ffuf -w /path/to/wordlist.txt:FUZZ -u https://FUZZ.url.com

Filtering => ffuf -w /path/to/wordlist.txt:FUZZ -u https://url/FUZZ -fs 900

Parameter Fuzzing GET => ffuf -w /path/to/wordlist.txt:FUZZ -u https://url/page.php?FUZZ=key

Parameter Fuzzing POST => ffuf -w /path/to/wordlist.txt:FUZZ -u https://url/page.php -X POST -d 'FUZZ=key' -H 'Content-Type: application/x-www-form-urlencoded' 
```


### gobuster

```
VHost Fuzzing => gobuster vhost -w /path/to/wordlist.txt -u http://academy.htb:PORT/ --append-domain

Sub Domain Fuzzing => gobuster dns -w /path/to/wordlist.txt -d http://academy.htb:PORT

Directory Fuzzing => gobuster dir -w /path/to/wordlist.txt -u http://academy.htb:PORT

File Fuzzing => gobuster dns -w /path/to/wordlist.txt -d http://academy.htb:PORT -x php,phps,php7,html...
```

