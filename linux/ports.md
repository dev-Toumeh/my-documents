## To check ports in Linux, you can use the netstat or ss commands. Here's how:
- netstat -tuln
- ss -tuln

## check which program is using a specific port
install `sudo apt-get install lsof`
- sudo lsof -i :<port_number>
