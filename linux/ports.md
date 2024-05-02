## install packages
- sudo apt install nmap
- sudo apt install lsof
- sudo apt install net-tools

## To check ports in Linux, you can use the netstat or ss commands. Here's how:
- netstat -tuln
- ss -tuln

## check which program is using a specific port
- sudo lsof -i :<port_number>

## to check available ports for specific ip
- nmap -sT -p- 192.168.1.1

