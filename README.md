# BruteSpray

Created by: Shane Young/@x90skysn3k && Jacob Robles/@shellfail 

Inspired by: Leon Johnson/@sho-luv

Credit to Medusa: JoMo-Kun / Foofus Networks - http://www.foofus.net

#### Version - 1.5

# Demo

https://youtu.be/C-CVLbSEe_g

# Description
BruteSpray takes nmap GNMAP/XML output and automatically brute-forces services with default credentials using Medusa. BruteSpray can even find non-standard ports by using the -sV inside Nmap.  

<img src="http://i.imgur.com/k9BDB5R.png" width="500">



# Usage
First do an nmap scan with ```-oG nmap.gnmap``` or ```-oX nmap.xml```.

Command: ```python brutespray.py -h```

Command: ```python brutespray.py --file nmap.gnmap```

Command: ```python brutesrpay.py --file nmap.xml```

Command: ```python brutespray.py --file nmap.xml -i```

<img src="https://i.imgur.com/25rfMAB.png" width="450">

## Examples

#### Using Custom Wordlists:

```python brutespray.py --file nmap.gnmap -U /usr/share/wordlist/user.txt -P /usr/share/wordlist/pass.txt --threads 5 --hosts 5```

#### Brute-Forcing Specific Services:

```python brutespray.py --file nmap.gnmap --service ftp,ssh,telnet --threads 5 --hosts 5```

#### Specific Credentials:
   
```python brutespray.py --file nmap.gnmap -u admin -p password --threads 5 --hosts 5```

#### Continue After Success:

```python brutespray.py --file nmap.gnmap --threads 5 --hosts 5 -c```

#### Use Nmap XML Output

```python brutespray.py --file nmap.xml --threads 5 --hosts 5```

#### Interactive Mode

```python brutespray.py --file nmap.xml -i```

<img src="https://i.imgur.com/zBXEU33.png" width="600">

# Supported Services

* ssh
* ftp
* telnet
* vnc
* mssql
* mysql
* postgresql
* rsh
* imap
* nntp
* pcanywhere
* pop3
* rexec
* rlogin
* smbnt
* smtp
* svn
* vmauthd

# Changelog
* v1.5
    * added interactive mode
* v1.4
    * added ability to use nmap XML 
* v1.3
    * added the ability to stop on success
    * added the ability to reference custom userlists and passlists
    * added the ability to specify specific users & passwords
