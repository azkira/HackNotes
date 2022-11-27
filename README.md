# HackNotes 【第一】

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

## Learn From Walkthroughs
- https://www.hackingarticles.in/seppuku1-vulnhub-walkthrough/ (brute forcing basic authentication)
