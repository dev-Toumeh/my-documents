### install a local package using apt 
- sudo apt install ./path/to/package.deb

### stop a process
- Find and Kill by Name: 
    pkill process_name
- Find and Kill by PID:
   1. Find the process ID (PID): ps aux | grep process_name
   2. Kill the process using its PID: kill PID
   3. If it doesn't stop, force kill it: kill -9 PID 
